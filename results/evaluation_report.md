# Evaluation Report - Statistical POS-tagged PCFG Parser

Test set: 150 Daily Mirror sentences, 3364 tokens.

## Dataset

Trained on the labelled NLTK Penn Treebank (`nltk.corpus.treebank`), as the brief instructs. The Kaggle language-modelling file has no tags or trees and cannot be used.

## Tagging metrics

| Metric | Value |
|---|---|
| Token accuracy | 0.7949 |
| Macro F1 | 0.7367 |
| Weighted F1 | 0.7947 |
| Known-word accuracy | 0.9201 |
| OOV-word accuracy | 0.2027 |

## Parsing metrics

| Metric | Value |
|---|---|
| Full-parse coverage | 0.9733 (146/150) |
| Avg parse time (s) | 0.7366 |

## Per-tag detail

```
              precision    recall  f1-score   support

           $       1.00      1.00      1.00         3
          ''       0.89      0.89      0.89         9
           (       0.00      0.00      0.00         7
           )       0.00      0.00      0.00         7
           ,       1.00      1.00      1.00       126
           .       1.00      1.00      1.00       151
           :       1.00      1.00      1.00         9
          CC       1.00      1.00      1.00        95
          CD       1.00      0.64      0.78        58
          DT       1.00      1.00      1.00       306
          EX       1.00      1.00      1.00         2
          FW       0.00      0.00      0.00         1
          IN       0.98      0.97      0.97       346
          JJ       0.94      0.62      0.74       245
         JJR       0.67      0.77      0.71        13
         JJS       0.86      0.75      0.80         8
          MD       1.00      1.00      1.00        41
          NN       0.45      0.96      0.61       481
         NNP       0.95      0.35      0.51       413
        NNPS       0.50      1.00      0.67         3
         NNS       0.97      0.64      0.77       229
         POS       0.95      0.95      0.95        22
         PRP       1.00      1.00      1.00        39
        PRP$       1.00      1.00      1.00        27
          RB       0.91      0.83      0.87       104
         RBR       0.50      0.17      0.25         6
         RBS       0.00      0.00      0.00         1
          RP       0.67      0.80      0.73         5
          TO       1.00      1.00      1.00        87
          UH       0.00      0.00      0.00         1
          VB       0.81      0.71      0.76       110
         VBD       0.77      0.79      0.78        85
         VBG       0.89      0.65      0.75        88
         VBN       0.76      0.59      0.66        87
         VBP       0.67      0.62      0.64        29
         VBZ       0.92      0.86      0.89        95
         WDT       0.62      0.89      0.73         9
          WP       1.00      1.00      1.00         1
         WRB       1.00      1.00      1.00         7
          ``       1.00      1.00      1.00         8

    accuracy                           0.79      3364
   macro avg       0.77      0.74      0.74      3364
weighted avg       0.87      0.79      0.79      3364
```

## Note on PARSEVAL

Full bracketing (PARSEVAL) scores need hand-built gold parse *trees* for all 150 sentences, which is out of scope here; token-level tagging metrics plus parse coverage are the standard metrics reported.
