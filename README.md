# pdp-structure-llm-experiment
Controlled experiment testing how LLMs interpret ecommerce product pages depending on content structure (messy vs structured vs AI-friendly).

## Objective

This experiment tests how the structure of ecommerce product pages affects how large language models interpret and describe products.

The goal is to understand whether content structure improves:

- Accuracy
- Completeness
- Clarity
- Constraint awareness

## Experiment Design

The same product (WIKA A-10 pressure transmitter) was used to create multiple PDP versions:

- Version A: Typical ecommerce (paragraph-heavy, mixed information)
- Version B: Structured (clear sections, bullet points, separated specs)
- Version C: Structured + explicit context (AI-friendly wording)

Each version was tested in two formats:

- Plain text
- HTML (basic semantic structure only)

## Test Matrix

- A_text
- A_html
- B_text
- B_html
- C_text
- C_html

## Prompts

All versions were tested using the same prompts:

1. Summarise the product
2. Extract technical specifications
3. Identify use cases and limitations
4. Highlight key decision-making information

## Evaluation Criteria

Outputs were evaluated based on:

- Accuracy
- Completeness
- Clarity
- Constraint awareness

## Goal

This experiment aims to understand how PDP content should be structured to improve interpretation by LLMs and AI search systems.

## Notes

This is a controlled test. The underlying product information remains the same across all versions. Only structure and wording change.
