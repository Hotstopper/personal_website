---
title: "BTC Regimes"
date: 2025-05-13
draft: false
---
{{< social "github" "https://github.com/Hotstopper/btc_halving" >}}

I used a Markov-switching (MS) model to classify the Bitcoin market into three distinct constant-mean regimes from 2012 to 2025. The results are as follows:

{{< figure src="btc_regime.png" alt="Bitcoin Regimes" caption="Log of Bitcoin's Daily Closing Prices" >}}
The colours red, grey, and green correspond to bearish, neutral, and bullish return regimes.

I find that periods of low economic uncertainty tend to coincide with bull regimes. This pattern reflects Bitcoin’s role as a risky asset, with investors allocating capital during stable macroeconomic conditions, leading to both higher expected returns and higher volatility, consistent with the MS model results. Such dynamics are compatible with EMH (efficient market hypothesis), as abnormal returns reflect time-varying risk premia rather than market inefficiency.

I overlayed the Bitcoin regimes identified above on 4 broad indicators of economic uncertainity. Probit regressions show that commodity markets significantly explain bull market regimes, and macroeconomic factors jointly explain regime transitions at p<0.01.

{{< figure src="gepu_regime.png" alt="Log of GEPU Index" caption="Log of GEPU Index" >}}
{{< figure src="spgsci_regime.png" alt="Log of S&P GS Commodity Index" caption="Log of S&P GS Commodity Index" >}}
{{< figure src="usd_regime.png" alt="Log of USD Index" caption="Log of USD Index" >}}
{{< figure src="vix_regime.png" alt="Log of CBOE Volatility Index" caption="Log of CBOE Volatility Index" >}}

For a more detailed and technical explanation, please check out my GitHub repository above, where you can find my 18-page report. In my report I also discuss market reactions to Bitcoin halving events.


