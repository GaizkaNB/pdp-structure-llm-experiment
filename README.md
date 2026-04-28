# PDP Structure and LLM Interpretation Experiment

Controlled experiment testing how LLMs interpret ecommerce product detail pages (PDPs) depending on content structure, wording, and embedded structured data.

## Objective

This project investigates how the structure of ecommerce product pages affects how large language models interpret, extract, and reason about product information.

The goal is to understand whether content structure improves:

- Accuracy
- Completeness
- Clarity
- Constraint awareness

## Phase 1: PDP Structure Experiment

The first experiment tested whether clearer PDP structure and more explicit natural language improved LLM interpretation.

The same product, the WIKA A-10 pressure transmitter, was used to create multiple PDP versions:

- Version A: Typical ecommerce (paragraph-heavy, mixed information)
- Version B: Structured (clear sections, bullet points, separated specs)
- Version C: Structured + explicit context (AI-friendly wording)

Each version was tested in two formats:

- Plain text
- HTML (basic semantic structure only)

### Phase 1 Test Matrix

- A_text
- A_html
- B_text
- B_html
- C_text
- C_html

### Phase 1 Finding

LLMs extracted specifications reasonably well from most versions, but they struggled more with constraints, relationships, and correct interpretation unless the page made those points explicit.

Structured content helped, but explicit natural language was especially important for use cases, limitations, and decision-making context.

## Phase 2: JSON vs Natural Language Extension

This follow-up extends the original experiment by testing whether embedded JSON metadata in the HTML source can improve LLM understanding compared with visible natural language content.

The core question is:

Can JSON metadata replace or complement explicit natural language for LLM interpretation?

### What Is Being Tested

The second phase evaluates two types of model behaviour:

- Extraction: Can the model correctly retrieve specifications and attributes?
- Interpretation: Can the model understand constraints, relationships, appropriate use cases, and when the product should not be used?

### Content Variants

The follow-up reuses the same product and base content from the first experiment, with JSON added as a new controlled variable.

- B_text: Structured content only
- B_html: Same visible content as B_text, plus embedded JSON in HTML
- C_text: Structured content plus explicit natural language context
- C_html: Same visible content as C_text, plus embedded JSON in HTML

### Input Modes

Each content variant is tested in two ways:

- Text-only input: rendered content only, with no HTML or JSON
- Full HTML input: complete HTML source, including embedded JSON where present

LLMs can only use the JSON when the full HTML source is included in the input.

### JSON Design

The same JSON structure and values should be used across all HTML variants so the test remains controlled.

The JSON should include:

- Technical specifications
- Applications
- Constraints and limitations
- Suitability and non-suitability signals

The JSON should not contain richer or different information than the intended experimental condition allows. Its role is to test whether machine-readable structure changes model performance, not whether extra hidden facts improve answers.

### Key Comparisons

The main comparisons for Phase 2 are:

- B_text vs B_html: Does JSON improve performance on its own?
- C_text vs C_html: Does JSON add value when the visible content is already explicit?
- B_html vs C_text: Can JSON replace explicit natural language?

### Hypothesis

The expected pattern is:

- JSON will improve structured extraction.
- Natural language will outperform JSON for interpretation and reasoning.
- The strongest performance may come from explicit natural language plus JSON together.

## Prompts

All versions were tested using the same prompts:

1. Summarise the product
2. Extract technical specifications
3. Identify use cases and limitations
4. Highlight key decision-making information

## Evaluation Criteria

Outputs are evaluated based on:

- Accuracy
- Completeness
- Clarity
- Constraint awareness

Constraint awareness is the key metric for the JSON extension because it captures whether the model understands limits, dependencies, and appropriate use rather than simply extracting facts.

## Goal

This project aims to understand how PDP content should be structured to improve interpretation by LLMs and AI search systems.

The extension specifically informs:

- Technical SEO strategy
- Schema and structured data usage
- PDP content design
- AI search optimisation
- LLM-based internal search systems

## Notes

This is a controlled test. The underlying product information should remain consistent across versions.

For Phase 1, only structure and wording change.

For Phase 2, the main variable is JSON presence in the HTML source. The visible text, prompts, and evaluation criteria should remain consistent within each comparison.
