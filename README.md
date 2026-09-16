# Anomaly-LR

**Industrial Anomaly Detection via Defect-Grounded Reasoning in Visual Latent Space**

> Code and data will be released here upon publication.

## Abstract

Industrial anomaly detection (IAD) is evolving beyond conventional detection and localization
toward multimodal inspection systems that can describe, explain, and reason about fine-grained
defects. Although recent multimodal large language model (MLLM)-based methods improve anomaly
understanding through explicit textual reasoning and auxiliary visual guidance, their intermediate
reasoning representations are rarely grounded in localized defect evidence, limiting their ability
to refine subtle anomaly cues. To address this, we propose Anomaly-LR, a defect-grounded latent
reasoning framework that first establishes a global understanding of the input and then
progressively refines anomaly-relevant representations in the latent space. We further construct
IAD-LR-7.6K, an instruction dataset containing 1,600 images across 38 industrial categories, with
global reasoning targets and region-level supervision for defect-grounded latent alignment.
Extensive experiments show that Anomaly-LR achieves state-of-the-art performance among methods of
comparable model scale on the MMAD benchmark.

## Results

Accuracy on the MMAD benchmark, averaged over the four source datasets and then over the seven
subtasks, both unweighted. `Anomaly Disc.` uses balanced accuracy over normal and abnormal images,
following the official implementation.

| Method | Scale | Shot | Average |
|---|---|---|---|
| AnomalyR1 | 3B | 1 | 76.96 |
| EMIT | 8B | 1 | 81.95 |
| AD-Copilot | 7B | 1 | 82.29 |
| InspectorGPT | 7B | 1 | 82.38 |
| AgentIAD | 3B | 1 | 82.88 |
| **Anomaly-LR** | **3B** | **0** | **86.00** |
| **Anomaly-LR** | **7B** | **0** | **87.15** |

Published entries are quoted from their source papers, which evaluate 1-shot on the full
benchmark (39,672 questions) with a retrieved reference image. Our models are 0-shot on the
32,059 questions whose images are disjoint from the training split, so the two protocols are not
directly comparable.

## Status

- [ ] Training code
- [ ] Evaluation code
- [ ] IAD-LR-7.6K instruction set
- [ ] Checkpoints

## Citation

```bibtex
@inproceedings{anomalylr2027,
  title     = {Industrial Anomaly Detection via Defect-Grounded Reasoning
               in Visual Latent Space},
  author    = {TODO},
  booktitle = {IEEE International Conference on Acoustics, Speech and
               Signal Processing (ICASSP)},
  year      = {2027}
}
```
