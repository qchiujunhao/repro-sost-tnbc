# Reproduction: SOST in triple-negative breast cancer

Source: YangX-BIDD/TNBC at commit d2cc7ad (Zenodo 10.5281/zenodo.18752090). Rerun 2026-11-14 with
Python 3.14, pandas 3.1.1, numpy 2.5.4, scipy 1.18.1, matplotlib 3.11.2, recorded with
[whatran](https://github.com/qchiujunhao/whatran). The record is in `analysis/`; `run.sh` reruns it and
`python3 analysis/whatran.py check` verifies it. The published figures are kept in `published/`.

## What reproduces

- **Figure 2** regenerates and is visually identical to the deposited PNG. Pearson r = 0.571 over 798
  pooled samples, as the README states.
- **Figure 1** regenerates and is visually identical to the deposited PNG (1x3 histograms, cutoff 50).

## What does not

- The README describes Figure 1 as a 4-panel figure with a unified cutoff of Q3 = 51.80 and positivity
  rates of 25% (TNBC), 9.6% (HER2+) and 82.8% (Luminal). No deposited script computes any of this: the
  script hard-codes a cutoff of 50 and prints 60.0%, 8.5% and 8.1%. The README also names two output
  files (`Figure_UnifiedCutoff_Clean.png`, `Figure_SubtypeDetails_Clean.png`) that the script does not
  write. The code that produced the README's numbers is not in the deposit.
