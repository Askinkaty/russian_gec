# russian_gec
Repository with models, datasets, and other experiments related to Russian GEC


## Update version of RULEC-GEC

A new version of RULEC-GEC can be obtained in several steps.

1. Get an original RULEC-GEC at https://github.com/arozovskaya/RULEC-GEC
2. Copy the original RULEC-GEC.text.M2 file
3. Use a patch file ```RULEC-GEC_updates.patch```. The copy of the test files will include correction updates.
   ```patch RULEC-GEC.copy_of_test.M2 RULEC-GEC_updates.patch```

Check out performance of a T5-based GEC model on a new test M2 file in the paper: 

 ```
@inproceedings{katinskaia-yangarber-2023-grammatical,
    title = "Grammatical Error Correction for Sentence-level Assessment in Language Learning",
    author = "Katinskaia, Anisia  and
      Yangarber, Roman",
    booktitle = "Proceedings of the 18th Workshop on Innovative Use of NLP for Building Educational Applications (BEA 2023)",
    month = jul,
    year = "2023",
    address = "Toronto, Canada",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.bea-1.41",
    pages = "488--502",
    abstract = "The paper presents experiments on using a Grammatical Error Correction (GEC) model to assess the correctness of answers that language learners give to grammar exercises. We explored whether a GEC model can be applied in the language learning context for a language with complex morphology. We empirically check a hypothesis that a GEC model corrects only errors and leaves correct answers unchanged. We perform a test on assessing learner answers in a real but constrained language-learning setup: the learners answer only fill-in-the-blank and multiple-choice exercises. For this purpose, we use ReLCo, a publicly available manually annotated learner dataset in Russian (Katinskaia et al., 2022). In this experiment, we fine-tune a large-scale T5 language model for the GEC task and estimate its performance on the RULEC-GEC dataset (Rozovskaya and Roth, 2019) to compare with top-performing models. We also release an updated version of the RULEC-GEC test set, manually checked by native speakers. Our analysis shows that the GEC model performs reasonably well in detecting erroneous answers to grammar exercises and potentially can be used for best-performing error types in a real learning setup. However, it struggles to assess answers which were tagged by human annotators as alternative-correct using the aforementioned hypothesis. This is in large part due to a still low recall in correcting errors, and the fact that the GEC model may modify even correct words{---}it may generate plausible alternatives, which are hard to evaluate against the gold-standard reference.",
}
```


