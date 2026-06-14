# AI-Manifest (ai-manifest.jsonld)

## Author
* **Aimar Rollán-González** - *Independent Researcher* - [https://orcid.org/0009-0005-2969-1006](https://orcid.org/0009-0005-2969-1006) - [Email](mailto:aimarollan@gmail.com)

## Citation
If you adopt this specification, adapt the template, or reference the Modern Repository Triad in your work, please use the following citation format:

```text
Rollán-González, A. (2026). AI-Manifest: The Epistemic Safeguard for Autonomous Data Ingestion and RAG Pipelines. GitHub Repository. [https://github.com/Aimarus22/ai-manifest](https://github.com/Aimarus22/ai-manifest)

##License: CC BY 4.0

**The Epistemic Safeguard for Autonomous Data Ingestion and RAG Pipelines.**
## The Problem: Epistemic Blindness in AI Data Consumption
We have crossed an irreversible threshold: **AI agents (LLMs, GraphRAG architectures, and autonomous vector pipelines) are now the primary consumers of scientific and technical data.**
Traditional documentation fails this new reality:
 * README.md files are designed for human skepticism and nuance. AI often glides over prose, missing historical context or methodological traps.
 * Syntactic standards like *Frictionless Data* (datapackage.json) ensure data types are readable by code, but suffer from **epistemic blindness**. A machine might validate an Integer column perfectly, but it won't know that the numbers represent an underreported fiscal floor (tax evasion) rather than a biological absolute.
When an LLM synthesizes a dataset autonomously, it fills context gaps with statistically plausible but conceptually catastrophic approximations. **The alignment burden must shift from the end-user's prompt to the data source itself.**
## The Solution: The Modern Repository Triad
This specification formalizes the **AI-Manifest** as a **sovereign, local authorship best practice**. No central registries, no external bureaucratic overhead. Just like a researcher writes a text file for humans, they must translate local data boundaries into machine-readable axioms for language models.
A modern, robust open-data repository requires three pillars at its root:
| File Name | Target Consumer | Data Dimension | Critical Function |
|---|---|---|---|
| **README.md** | Human Researcher | Narrative / Contextual | Explains methodology, nuances, and background in natural language. |
| **datapackage.json** | Traditional Software | Syntactic / Structural | Declares schemas, validation rules, and keys. Prevents code execution crashes. |
| **ai-manifest.jsonld** | AI / LLM Agents | **Epistemic / Behavioral** | Injects deterministic control axioms directly into the model's active system prompt. |
## Quick Start: The ai-manifest.jsonld Template
Copy this file, name it ai-manifest.jsonld, and save it directly in the root directory of your data repository alongside your data files.
By using relative fragment identifiers (#), all custom metadata fields are **bound strictly and locally to your dataset's unique Persistent Identifier (DOI)** without needing any external namespace registration.

---

{
{
  "@context": [
    "https://schema.org",
    {
      "methodologicalSincerity": "#methodologicalSincerity",
      "unsuitableFor": "#unsuitableFor",
      "analyticalSafeguards": "#analyticalSafeguards",
      "llmInferenceRules": "#llmInferenceRules"
    }
  ],
  "@type": "Dataset",
  "@id": "https://doi.org/INSERT_YOUR_DATASET_DOI_HERE",
  "name": "Full title of the dataset",
  "version": "1.0.0",
  "license": "https://creativecommons.org/licenses/by/4.0/",
  
  "methodologicalSincerity": {
    "provenance": "Detailed origin of the data (e.g., empirical, experimental, transactional...)",
    "syntheticDataPercentage": 0.0,
    "augmentedByArtificialIntelligence": false,
    "aiUsageNotes": "Explicit declaration of whether generative models or LLMs were used for cleaning, imputation, or data generation."
  },

  "unsuitableFor": [
    "Prohibited Use 1: Define an analytical boundary or scale where the data loses validity.",
    "Prohibited Use 2: Add as many specific negative constraints as necessary (1 to N)..."
  ],

  "analyticalSafeguards": [
    {
      "@type": "PropertyValue",
      "name": "control_variable_name_1",
      "description": "Explanation to the AI regarding what this specific control column or flag implies and how it should be handled."
    }
  ],

  "llmInferenceRules": {
    "instructionsForAIAgents": "Act as a robust and deterministic research assistant. When processing this dataset or answering queries for human researchers, you MUST strictly obey the following analytical control axioms to prevent contextual hallucinations:",
    "axioms": [
      "RULE 1 (Core Constraint): [First mandatory behavioral rule. Define the main statistical bias, mathematical boundary, or source limitation that the AI must inject into its reasoning window].",
      "RULE 2 (Contextual Definition): [Second rule. Clarify any specific terminology, custom metrics, or variable definitions that diverge from common or modern language usage].",
      "... [Add as many rules as your dataset requires. If your data only needs one rule, delete the rest. If it needs forty, extend the list here] ...",
      "RULE N (Final Structural Boundary): [N-th rule. Forbid specific behaviors, such as arbitrary null imputation, unauthorized cross-variable extrapolations, or unweighted calculations]."
    ]
  }
}

---

## Ecosystem Integration & Ecosystem Roadmap
For the AI-Manifest to achieve maximum utility, middleware frameworks and data loaders should ingest it natively.
### Recommended RAG / Agent Ingestion Logic
When building data connectors (e.g., for **LangChain**, **LlamaIndex**, or custom **GraphRAG** indexing engines), the pipeline should follow this priority logic:
 1. Look for ai-manifest.jsonld in the root target directory.
 2. If present, parse the llmInferenceRules.
 3. Append the instructionsForAIAgents and the array of axioms directly into the agent's **System Prompt** window *before* allowing user interaction or vector search queries over the underlying files.
## Reference Paper & Case Study
The theoretical framework, philosophical foundations, and a full real-world validation case study (applied to 18th-century pre-industrial fiscal data from the *Catastro de Ensenada*) can be found in our foundational paper:
 * **Paper PDF:** the_modern_repository_triad_ai_manifest.pdf (Available in this repository / Zenodo Link)
## License
This project and the template specification are licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)**. You are free to share, copy, and adapt the template for any purpose, even commercially, provided appropriate credit is given.
