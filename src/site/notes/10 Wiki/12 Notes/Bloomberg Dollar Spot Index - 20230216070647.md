---
aliases: Bloomberg Dollar Spot Index
created: 20230216070653
dg-publish: true
tags:
- wiki/meta/random
updated: 20230216070653
---
# Bloomberg Dollar Spot Index
---
The **Bloomberg Dollar Spot Index** (BBDXY) tracks the performance of a basket of 10 global currencies against the U.S. dollar.

The index rebalances once a year to incorporate new data from:
- The annual survey of **major trading partners** versus the U.S. dollar as reported by the Federal Reserve.
- The triennial survey of **most liquid currencies** as reported by the Bank of International Settlements (BIS).

## Composition
![Pasted image 20221111180344.png](/img/user/90%20Meta/Attachments/Pasted/Pasted%20image%2020221111180344.png)

## Calculation
1.  **Identify the top 20 currencies in terms of trading activity versus the underlying currency.** For the U.S. dollar, this is as defined by the Federal Reserve in its Broad Index of the Foreign Exchange Value of the Dollar.
2.  **Identify the top 20 currencies from the [Triennial Central](https://www.bis.org/statistics/rpfx19.htm)** **Bank Survey of Foreign Exchange and Derivatives** **Market Activity.** Specific information about foreign exchange turnover can be found [here](https://www.bis.org/statistics/rpfx19_fx.htm).
3.  **Select the top 10 currencies of both lists, but exclude any pegged currencies.** For example, currencies pegged to the U.S. dollar (such as the Hong Kong dollar or Saudi riyal) are removed for the Bloomberg Dollar Spot Index.
4.  **Assign a preliminary weight for each currency based on its trade weight and liquidity weight.** 
5.  **Cap the exposure of Chinese renminbi and remove smaller currency positions,** defined as any position that has a weight of less than 2%.
6.  Voila! BBDXY calculation complete!

![Pasted image 20221111180526.png](/img/user/90%20Meta/Attachments/Pasted/Pasted%20image%2020221111180526.png)





###### META
Status:: #wiki/notes/mature 
Plantations:: [[10 Wiki/13 Plantations/Finance - 20230221102436\|Finance - 20230221102436]]
References:: [[10 Wiki/14 References/Other/Babypips - 20230122084125\|Babypips]]
