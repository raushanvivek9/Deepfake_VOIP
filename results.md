# Results

| Condition | EER | AUC | Accuracy | F1 |
|---|---|---|---|---|
| Clean | 0.0296 | 0.9965 | 0.9729 | 0.9793 |
| VoIP-degraded (codec + noise) | 0.1482 | 0.9251 | 0.8568 | 0.8879 |

## Data
- Fake: provided ~40h set, cleaned (corrupt/silence/non-speech removed), balanced by duration.
- Real: LibriSpeech train-clean-100, cleaned + balanced by duration, speaker-disjoint split.

## VoIP degradation
Random Opus/G.711 codec round-trip + 8kHz downsample round-trip + MUSAN noise at random SNR in {0,5,10,15} dB.

## Threshold
0.5 on P(fake) (default). Consider reporting the val-set EER-point threshold for a stricter comparison.
