# Evaluation Report - Statistical POS-tagged PCFG Parser

Test set: 150 Daily Mirror sentences, 2029 tokens.

## Dataset

Trained on the labelled NLTK Penn Treebank (`nltk.corpus.treebank`), as the brief instructs. The Kaggle language-modelling file has no tags or trees and cannot be used.

## Tagging metrics

| Metric | Value |
|---|---|
| Token accuracy | 1.0000 |
| Macro F1 | 1.0000 |
| Weighted F1 | 1.0000 |
| Known-word accuracy | 1.0000 |
| OOV-word accuracy | 1.0000 |

## Parsing metrics

| Metric | Value |
|---|---|
| Full-parse coverage | 1.0000 (150/150) |
| Avg parse time (s) | 0.1438 |

## Per-tag detail

```
              precision    recall  f1-score   support

           ,       1.00      1.00      1.00        20
           .       1.00      1.00      1.00       150
          CC       1.00      1.00      1.00        42
          CD       1.00      1.00      1.00        17
          DT       1.00      1.00      1.00       256
          EX       1.00      1.00      1.00         1
          IN       1.00      1.00      1.00       189
          JJ       1.00      1.00      1.00       108
         JJR       1.00      1.00      1.00         7
         JJS       1.00      1.00      1.00         3
          MD       1.00      1.00      1.00        25
          NN       1.00      1.00      1.00       572
         NNP       1.00      1.00      1.00        84
        NNPS       1.00      1.00      1.00        12
         NNS       1.00      1.00      1.00        92
         POS       1.00      1.00      1.00         7
         PRP       1.00      1.00      1.00        17
        PRP$       1.00      1.00      1.00        16
          RB       1.00      1.00      1.00        52
         RBR       1.00      1.00      1.00         1
          RP       1.00      1.00      1.00         2
          TO       1.00      1.00      1.00        51
          VB       1.00      1.00      1.00        60
         VBD       1.00      1.00      1.00        61
         VBG       1.00      1.00      1.00        34
         VBN       1.00      1.00      1.00        42
         VBP       1.00      1.00      1.00        19
         VBZ       1.00      1.00      1.00        82
         WDT       1.00      1.00      1.00         3
          WP       1.00      1.00      1.00         1
         WRB       1.00      1.00      1.00         3

    accuracy                           1.00      2029
   macro avg       1.00      1.00      1.00      2029
weighted avg       1.00      1.00      1.00      2029
```

## Note on PARSEVAL

Full bracketing (PARSEVAL) scores need hand-built gold parse *trees* for all 150 sentences, which is out of scope here; token-level tagging metrics plus parse coverage are the standard metrics reported.
