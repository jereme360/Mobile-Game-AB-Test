# Cookie Cats A/B Test Analysis: Gate Placement and Player Retention
## Introduction
Cookie Cats is a popular mobile puzzle game developed by Tactile Entertainment.  A key aspect of the game is the use of "gates" – levels where players are forced to wait a non-trivial amount of time or make an in-app purchase to continue. These gates serve two purposes:

- Monetization: Encouraging in-app purchases.
- Player Engagement: Providing breaks that can prolong enjoyment and prevent burnout.
The product team is interested in optimizing the placement of these gates to maximize player retention, a critical metric for the game's success. This analysis focuses on an A/B test where the first gate was moved from level 30 to level 40.

## Experiment Design
- Control Group: Players who encountered the first gate at level 30 (gate_30).
- Treatment Group: Players who encountered the first gate at level 40 (gate_40).
- Primary Metric: 1-day and 7-day retention rates.

## Methodology
To evaluate the impact of gate placement on retention, I employed a bootstrapping approach. This involved:
- Resampling: Repeatedly sampling (with replacement) from the original dataset to create multiple "bootstrap samples."
- Mean Calculation: Calculating the mean retention rate for each bootstrap sample within each group (gate_30 and gate_40).
- Distribution: Constructing a distribution of these bootstrapped means.
- Kernel Density Estimation (KDE): Using KDE to visualize the distribution of bootstrapped means for each group, allowing for a comparison of their overlap and potential differences.

## Conclusion
By analyzing the bootstrapped distributions and observing the overlap (or lack thereof) in the KDE plot, you can draw conclusions about the effect of moving the first gate from level 30 to level 40. This will inform the product team's decision on the optimal gate placement strategy for maximizing player retention.
