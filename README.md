# Synthetic4Health: Generating Annotated Synthetic Clinical Letters

A system to generate annotated, synthetic, de-identified clinical letters while protecting entities and document structure. 

This work presents a system for generating synthetic, de-identified clinical letters that are distinguishable from the originals, while preserving entities and document structures. We employed a hybrid approach, combining rule-based methods and named entity recognition (NER), to safeguard necessary information while exploring different models. We investigated various masking ratios and strategies based on token types (e.g., POS tags, stopwords) to balance diversity and similarity in synthetic letters. Our results demonstrate that this system produces high-quality synthetic clinical letters and is effective in protecting key information using encoder-only models, based on NER, POS tags, and stopword status.

Paper available at: (https://aclanthology.org/2025.privatenlp-main.6/)
---
> **Note:** Due to data use restrictions, the MIMIC-IV-Note dataset (v2.2) cannot be publicly shared in this repository. However, it is available to credentialed users via PhysioNet (https://physionet.org/content/mimic-iv-note/2.2/) upon completion of the required data use agreement and approval process.

---
# Abstract 
Since clinical letters contain sensitive information, clinical-related datasets can not be widely applied in model training, medical research, and teaching. This work aims to generate reliable, various, and de-identified synthetic clinical letters. We explored different pre-trained language models (PLMs) for masking and generating text to achieve this goal. After that, we worked on Bio\_ClinicalBERT, a high-performing model, and experimented with different masking strategies. Both qualitative and quantitative methods were used for evaluation. A downstream task, Named Entity Recognition (NER), was also implemented to assess the usability of these synthetic letters.
The results indicate that 
1) encoder-only models outperform encoder-decoder models.
2) Among encoder-only models, those trained on general corpora perform comparably to those trained on clinical data when clinical information is preserved.
3) Additionally, preserving clinical entities and document structure better aligns with our objectives than simply fine-tuning the model.
4) Furthermore, different masking strategies can impact the quality of synthetic clinical letters. Masking stopwords has a positive impact, while masking nouns or verbs has a negative effect.
5) For evaluation, BERTScore should be the primary quantitative evaluation metric, with other metrics serving as supplementary references.
6) Contextual information does not significantly impact the models' understanding, so the synthetic clinical letters have the potential to replace the original ones in downstream tasks.
7) Although the model occasionally generates hallucinated content, it appears to have little effect on overall clinical performance.

# cite us:


```bibtex
@inproceedings{ren-etal-2025-beyond,
    title = "Beyond Reconstruction: Generating Privacy-Preserving Clinical Letters",
    author = "Ren, Libo  and
      Belkadi, Samuel  and
      Han, Lifeng  and
      Del-Pinto, Warren  and
      Nenadic, Goran",
    editor = "Habernal, Ivan  and
      Ghanavati, Sepideh  and
      Jain, Vijayanta  and
      Igamberdiev, Timour  and
      Wilson, Shomir",
    booktitle = "Proceedings of the Sixth Workshop on Privacy in Natural Language Processing",
    month = apr,
    year = "2025",
    address = "Albuquerque, New Mexico",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.privatenlp-main.6/",
    pages = "60--74",
    ISBN = "979-8-89176-246-6"
}
