---
title: "Hong Kong Election Analysis"
date: 2025-04-07
draft: false
---
{{< social "github" "https://github.com/Hotstopper/hk_election" >}}

# 2019年香港區議會選舉

Hong Kong’s 2019 District Council election marked a turning point in the city’s political history.  Across 18 districts, pan-democratic candidates won over 80 % of all seats (57% of the popular vote) in a political landslide.

But the scale of that victory raises a more subtle question: which communities moved the most, and why?

To answer this, I combined official election returns from 2015 and 2019 with demographic data from the 2021 Census, creating a district-level dataset of age, education, income, and population structure.

I then ran a series of weighted regressions on 2019 vote shares, and then on the change in vote share between 2015 and 2019. I wanted to see whether certain demographics were systematically associated with political preference. 

---

## Age and Political Support

{{< figure src="fig_age_2019.png" alt="Figure of Age Distribution on Pan-Dem Vote Shares in 2019" caption="Effect of Age Composition on Pan-Dem Vote Share" >}}

The positive elderly coefficient is counterintuitive, but likely reflects enduring support for moderate pan-democrats such as the Democratic Party, which historically drew votes from older, middle-class professionals rather than younger activists.

{{< figure src="fig_age_swing.png" alt="Figure of Age Distribution on Pan-Dem Vote Swings from 2015 to 2019" caption="Effect of Age Composition on Pan-Dem Vote Swing" >}}

When we look at the change in vote share between 2015 and 2019, the picture flattens.

The uniformly positive pattern also reflects the choice of baseline. The omitted 0–14 age group corresponds to child-heavy districts, typically newer and more family-oriented areas, where the disruption and uncertainty of the protests may have dampened support for the movement. Relative to these, all adult-dominant districts appear more pro-democratic in the change.

Although none of the coefficients are statistically significant, the youngest cohort (15–24) shows the largest point estimate, suggesting that youth-heavy districts may have experienced somewhat stronger mobilisation.

The popular image of the movement as a purely youth-led revolt may capture patterns of participation and activism, but not of electoral behaviour. In voting terms, the 2019 swing was broad-based across generations, with mobilisation likely more intense in younger areas but widespread across the electorate as a whole.

---
## Income Strucure and Political Support

Income tells a more distinct story.

{{< figure src="fig_income_2019.png" alt="Figure of Income Distribution on Pan-Dem Vote Shares in 2019" caption="Effect of Income on Pan-Dem Vote Share" >}}

Pan-democratic support peaks in middle-income districts (roughly HKD 30,000–60,000 per month) and declines toward both the low and high ends.

The pattern resembles an inverted U-shape, consistent with a broad middle-class coalition: affluent enough to value civil liberties and not preoccupied with day-to-day survival, yet not so elite as to be insulated by wealth, mainland connections, or the gains of China’s earlier growth.

However, none of these coefficients are statistically significant, so this curvature should be interpreted as a suggestive pattern rather than a definitive relationship.

{{< figure src="fig_income_swing.png" alt="Figure of Income Distribution on Pan-Dem Vote Swings from 2015 to 2019" caption="Effect of Income on Pan-Dem Vote Swing" >}}

When we look at the change in vote share, most income brackets show small, positive coefficients, with the lowest group slightly negative, but all are well within the range of statistical uncertainty.

This implies that the 2019 swing toward pan-democrats was broadly uniform across income levels, rather than driven by a specific class.

The modest differences between groups suggest that the inverted-U shape observed in 2019 was not created by the protests themselves. Instead, the entire income–vote relationship appears to have shifted upward—middle-income districts remained relatively more pan-democratic, but support rose across the spectrum.

If anything, poorer districts moved slightly less, while higher-income areas maintained their earlier positions, or shifted away from pro-establishment camps.

Overall, the 2019 election reflected a city-wide rise in pan-democratic sentiment rather than a new class alignment.

---

## Geographic Swing Patterns

{{< figure src="fig_region_2019.png" alt="Figure of Geographical Distribution on Pan-Dem Vote Shares in 2019" caption="Regional Differences in Pan-Dem Vote Share" >}}

Even after accounting for demographics, regional differences remain visible.

Kowloon and the New Territories show higher pan-democratic vote shares than Hong Kong Island, which serves as the baseline.

These areas combine dense new-town populations, strong transport connectivity, and strong local networks.

{{< figure src="fig_region_swing.png" alt="Figure of Geographical Distribution on Pan-Dem Vote Swings from 2015 to 2019" caption="Regional Differences in Pan-Dem Vote Swing" >}}

Between 2015 and 2019, the regional differences in swing are smaller and statistically insignificant, indicating that the political realignment was broadly shared across space.

The small negative coefficient for NT Urban relative to Hong Kong Island suggests that areas which were already strongholds in 2015 had less room to swing further, while weaker regions caught up.

In effect, the protest wave narrowed the regional gap rather than creating new ones, implying that the surge in 2019 was territory-wide. It was an upward shift of the entire political landscape rather than a geographically concentrated swing.

___

## Education and Gender
Education remains one of the strongest and most consistent predictors of pan-democratic support.

In 2019, districts with larger shares of degree-holders were markedly more pan-democratic, even after controlling for income and age.
The relationship is both statistically significant and substantively large, suggesting that education captures deeper civic and informational divides. This structural gap long predates 2019, but the protests appear to have reinforced it rather than diminished it.

Gender, by contrast, shows no systematic pattern.

The male share of the population is positively signed in both the 2019 regression and the vote-swing model, but neither coefficient is significant.

This indicates that the 2019 shift was not gendered: men and women moved similarly, and overall pan-democratic support does not differ meaningfully across districts by gender composition.


For more details, feel free to visit my GitHub repository linked above.

---