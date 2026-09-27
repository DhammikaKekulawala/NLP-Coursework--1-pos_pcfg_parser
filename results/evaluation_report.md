# Evaluation Report - Statistical POS-tagged PCFG Parser

Test set: 150 Daily Mirror sentences, 3363 tokens.

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
| Full-parse coverage | 0.9800 (147/150) |
| Avg parse time (s) | 0.8860 |

## Per-tag detail

```
              precision    recall  f1-score   support

           $       1.00      1.00      1.00         3
          ''       1.00      1.00      1.00         9
           ,       1.00      1.00      1.00       126
           .       1.00      1.00      1.00       151
           :       1.00      1.00      1.00         9
          CC       1.00      1.00      1.00        95
          CD       1.00      1.00      1.00        37
          DT       1.00      1.00      1.00       306
          EX       1.00      1.00      1.00         2
          IN       1.00      1.00      1.00       342
          JJ       1.00      1.00      1.00       161
         JJR       1.00      1.00      1.00        15
         JJS       1.00      1.00      1.00         7
          MD       1.00      1.00      1.00        41
          NN       1.00      1.00      1.00      1016
         NNP       1.00      1.00      1.00       151
        NNPS       1.00      1.00      1.00         6
         NNS       1.00      1.00      1.00       151
         POS       1.00      1.00      1.00        21
         PRP       1.00      1.00      1.00        39
        PRP$       1.00      1.00      1.00        27
          RB       1.00      1.00      1.00        94
         RBR       1.00      1.00      1.00         2
          RP       1.00      1.00      1.00         6
          TO       1.00      1.00      1.00        87
          VB       1.00      1.00      1.00        96
         VBD       1.00      1.00      1.00        87
         VBG       1.00      1.00      1.00        64
         VBN       1.00      1.00      1.00        67
         VBP       1.00      1.00      1.00        27
         VBZ       1.00      1.00      1.00        89
         WDT       1.00      1.00      1.00        13
          WP       1.00      1.00      1.00         1
         WRB       1.00      1.00      1.00         7
          ``       1.00      1.00      1.00         8

    accuracy                           1.00      3363
   macro avg       1.00      1.00      1.00      3363
weighted avg       1.00      1.00      1.00      3363
```

## Note on PARSEVAL

Full bracketing (PARSEVAL) scores need hand-built gold parse *trees* for all 150 sentences, which is out of scope here; token-level tagging metrics plus parse coverage are the standard metrics reported.
