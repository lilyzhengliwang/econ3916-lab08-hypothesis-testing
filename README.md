# econ3916-lab08-hypothesis-testing

# Hypothesis Testing — Is Job Training Worth It?

## Objective
I tested whether a randomized job training program raised 1978 earnings, and checked how large and how reliable that effect is.

## Methodology
- Loaded the LaLonde NSW job training experiment (445 people: 185 trainees and 260 controls).
- Ran a one-sample t-test and a two-sample Welch's t-test on 1978 earnings.
- Wrote Welch's t-statistic as a function, `welch_t()`, and checked it against scipy on the full sample and on five subgroups.
- Computed Cohen's d to judge the size of the effect, not only whether it is significant.
- Ran a power analysis for this study and for the sample size needed to detect d = 0.3.
- Tested the treatment effect in 5 overlapping demographic subgroups, then applied Bonferroni and Benjamini-Hochberg corrections.
- Simulated p-value distributions for when the null is true and when it is false.

## Key Findings
- Trainees earned $1,794 more in 1978 than controls (Welch's t = 2.6741, p = 0.0079), a Cohen's d of 0.2727. That is a small effect, so the result is statistically significant but not large.
- 2 of the 5 subgroup effects were significant before correction, and 1 was significant after Bonferroni. It was the same subgroup (Black participants) under Benjamini-Hochberg.
- The subgroups overlap, so they are not five independent tests, and the subgroup with the fewest people (Hispanic participants) is too small to say much.
- A significant result alone does not show the program is worth funding. I would also need the cost per participant.
