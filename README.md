# Sylheti-CAP: Context-Aware Prompting for Bangla ↔ Sylheti Machine Translation

Large Language Models (LLMs) have demonstrated strong translation abilities through prompting, even without task-specific training. However, their effectiveness in dialectal and low-resource contexts remains underexplored. This study presents the first systematic investigation of LLM-based Machine Translation (MT) for Sylheti, a dialect of Bangla that is itself low-resource.

We evaluate five advanced LLMs (GPT-4.1, GPT-4.1-mini, LLaMA 4, Grok 3, and Deepseek V3.2) across both translation directions (Bangla ↔ Sylheti), and find that these models struggle with dialect-specific vocabulary. To address this, we introduce **Sylheti-CAP (Context-Aware Prompting)**, a three-step framework that embeds a linguistic rulebook, dictionary (core vocabulary and idioms), and authenticity check directly into prompts.

Extensive experiments show that Sylheti-CAP consistently improves translation quality across models and prompting strategies. Both automatic metrics and human evaluations confirm its effectiveness, while qualitative analysis reveals notable reductions in hallucinations, ambiguities, and awkward phrasing—establishing Sylheti-CAP as a scalable solution for dialectal and low-resource MT.

<p align="center">
  <b><font color="red">This paper has been accepted at BNLP @ AACL.</font></b>
  <img src="https://img.shields.io/badge/Accepted-BNLP%20@%20AACL-red" alt="Accepted at BNLP @ AACL">
</p>


---

## Sylheti-CAP Prompting Framework

Sylheti-CAP is a three-stage prompting framework:

1. **Linguistic Rulebook Integration**  
   Inject Sylheti-specific grammatical and morphological rules into the prompt so the LLM respects dialectal structure.

2. **Bilingual Lexicon & Idiom Dictionary**  
   Provide a curated Bangla–Sylheti lexicon (core vocabulary, function words, and idioms) to guide lexical choice and reduce hallucinations.

3. **Authenticity & Fluency Check**  
   Ask the model to self-check whether the output sounds natural, dialect-appropriate, and faithful to the source, then revise if needed.


## Sylheti-CAP Framework

<img src="Proposed_prompt.png" alt="Overview of the Sylheti-CAP prompting framework" width="320">

## Contact

**Authors**  
Tabia Tanzin Prama¹³⁵, Christopher M. Danforth¹²³⁴, Peter Sheridan Dodds¹²³⁵⁶  

**Affiliations**  
¹ Computational Story Lab  
² Vermont Complex Systems Institute  
³ Vermont Advanced Computing Center  
⁴ Department of Mathematics and Statistics  
⁵ Department of Computer Science  
University of Vermont, Burlington, VT 05405, USA  
⁶ Santa Fe Institute, 1399 Hyde Park Rd, Santa Fe, NM 87501, USA  

**Corresponding author:** Tabia Tanzin Prama — 📧 tprama@uvm.edu
