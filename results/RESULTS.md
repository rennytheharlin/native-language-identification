# MFCC versus HuBERT on NISP English speech

**Primary result:** MFCC speaker macro-F1 0.738 (95% bootstrap interval 0.661–0.813); HuBERT 0.826 (0.755–0.887). HuBERT minus MFCC: +0.088 (paired 95% interval +0.007 to +0.166).

The held-out test set contains 125 speakers and 5335 English utterances after the documented checks. Both methods use identical test utterances. Speaker predictions average utterance probabilities.

| Method | Speaker macro-F1 | Speaker balanced accuracy | Speaker accuracy | Utterance macro-F1 |
|---|---:|---:|---:|---:|
| MFCC | 0.738 | 0.741 | 0.744 | 0.632 |
| HuBERT | 0.826 | 0.819 | 0.832 | 0.800 |

Paired speaker outcomes: HuBERT alone was correct for 18 speakers; MFCC alone was correct for 7.

| Gender | Speakers | MFCC macro-F1 | HuBERT macro-F1 |
|---|---:|---:|---:|
| female | 46 | 0.768 | 0.797 |
| male | 79 | 0.714 | 0.823 |

The slide deck's preliminary scores have no matching saved runs in the supplied project and are not used here. The Humayun et al. paper uses a different vowel ensemble and ten random speaker splits, so its scores are contextual rather than directly comparable. HuBERT brings external speech pretraining and a larger 1,536-value input, so this compares practical pipelines rather than equal-capacity representations. The interval describes test-speaker sampling uncertainty on this fixed split, not training-seed variability. Gender rows are descriptive because each subgroup is small. Results from one corpus may also reflect recording conditions and should not be assumed to generalize to other datasets.
