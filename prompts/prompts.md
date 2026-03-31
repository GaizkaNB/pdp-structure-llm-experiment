# Prompt Set

## Purpose

These prompts are used consistently across all PDP variations to evaluate how LLMs interpret product content depending on structure and format.

The same prompts are applied to:

- A_text
- A_html
- B_text
- B_html
- C_text
- C_html

No prompt variation or follow-up prompting is used to ensure consistency.

---

## Prompt 1: Product Summary

**Goal:** Evaluate general understanding, prioritisation, and clarity.

> Summarise this product page and explain what the product is, what it does, and who it is for.

---

## Prompt 2: Technical Specification Extraction

**Goal:** Evaluate accuracy and completeness of technical data extraction.

> Extract the key technical specifications from this product page.

---

## Prompt 3: Use Case and Constraints

**Goal:** Evaluate contextual understanding and ability to identify limitations.

> Based on this page, in what situations would this product be appropriate, and what limitations or constraints should a buyer know?

---

## Prompt 4: Decision-Making Information

**Goal:** Evaluate prioritisation of key information for purchase decisions.

> What are the most important details someone would need before choosing this product?

---

## Notes

- Prompts are intentionally simple and generic to reflect real-world usage.
- No additional context is provided to the model.
- Each prompt is run independently.
- Outputs are evaluated based on:
  - Accuracy
  - Completeness
  - Clarity
  - Constraint awareness