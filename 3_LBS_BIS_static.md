# Bank Exposures - static visualization


Jorge Guerrero

## Description

Explore the network of bank exposures: from reporting country → counterparty country via the Locational banking statistics (LBS) published by the Bank for International Settlement (BIS) to assess which countries have hihger expositions. The final visualization attemps to explore in an easy language and intuitive lenaguage the global finane interconnections. 

## Data
The locational banking statistics (LBS) measure international banking activity from a residence perspective, focusing on the location of the banking office.  The LBS capture the outstanding claims (financial assets) and liabilities of internationally active banks located in reporting countries on counterparties residing in more than 200 countries. Banks record their positions on an unconsolidated basis, including intragroup positions between offices of the same banking group. The LBS capture around 95% of all cross-border banking activity.

The data is published in US dollars, quarterly, with timeseries since 1980 and it is accesible through API. I am planning to use timeseries since 2000 and end-date of 2024. This dataset contains the cross-country expositions.

In particular, for the static visualization we are working with a subset of the series, filtered in the website and retrieved with the API specific link.

Applied filters to the series:
1. **Time and frequency:** quarterly last 25 years (Q4-2000 to Q3-2025)
2. **Units:** outstanding amounts in USD
3. **Balance sheet position:** claims (what the banks lend) and liabilities (what the banks borrowed)
4. **Instruments:** A- all intruments (include loans, deposits, derivatives)
5. **Currency denominated (nominal):** TO1 - all currencies
6. **Currency type:** A - all currencies (add domestic, foreign and unclassified)
7. **Parent country:** 5J - all countries
8. **Reporting bank type:** A - all reporting banks and institutions (include domestic and foreign)
9. **Reporting country:** distinct values by ISO-2 country code
10. **Counterparty sector:**  A - all sectors (include banks,non financial corporations, NBFI, government, Households, etc.)
11. **Counterparty country:** distinct values by ISO-2 country code
12. **Position type:** cross border

The work acomplishes to illustrate that:

 - Money moves across borders more than ever before. Nowadays, banks and investors in one country routinely lend to or borrow from others. This web of cross-border connections means that financial problems in one place can quickly spread elsewhere — for example, when a major lender faces losses and reduces funding to other markets.
 - International borrowing and lending have grown steadily since 2000, reflecting growing integration despite the temporary pullback after the 2008 global financial crisis. Overall, the world lends more than it borrows, yet the distribution of who holds those positions has changed notably in the past decade.
 - Countries play different roles in this system. Some are net borrowers or lenders, often wealthier countries remain key suppliers of capital, while many developing countries are net recipients.
 - Managing global financial risks requires diversification. When banks or governments depend too heavily on the same few countries for funding, they become more vulnerable to global shocks. A handful of financial centers — the US, UK, and Germany — act as central hubs in this network, making them both sources of stability and potential channels for contagion.

 ![](static-viz/cross_border_finance_info.svg)



## Reproduce graphs
To reproduce the visualizations included in the infographic you could run the jupyter notebook:
"../src/milestone_2.2.ipynb"



## Data Sources

Bank for International Settlements. (2025). Locational Banking Statistics (LBS). BIS Data Portal. https://data.bis.org/topics/LBS