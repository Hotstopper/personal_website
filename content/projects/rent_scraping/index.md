---
title: "Webscraping Hong Kong Rental Transactions"
date: 2024-08-22
draft: false
---
{{< social "github" "https://github.com/Hotstopper/centaline_rent_scraping" >}}

In 2024, I was tasked with analysing the real estate industry in Hong Kong. Our original database only had around 200 transactions. So I scraped rent prices for around 9000 past transactions on Centaline from May 2024 to August 2024 using Selenium. 

{{< figure src="centaline_chinese.png" alt="Centaline Website (Chinese)" caption="Centaline Rental Transactions (Chinese)" >}}
{{< figure src="centaline_english.png" alt="Centaline Website (English)" caption="Centaline Rental Transactions (English)" >}}

We were mostly interested in the unit rate, so I used Selenium to identify the unit rate by XPATH, and saved them in a csv file.

For more details, feel free to visit my GitHub repository linked above.

---