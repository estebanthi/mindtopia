---
aliases: Casinos Bonuses Theory
created: 20230129064450
dg-publish: true
tags:
- wiki/my-thinking
- wiki/meta/favorite
updated: 20230129064450
---
# Casinos Bonuses Theory
---
It's mathematically possible to have an edge over [[Casino\|Casinos]] giving bonuses.

I won't explain how casino bonuses work, but it's a prerequisite to understand the Casinos Bonuses Theory.

## Definitions
Let's start with the definitions:
- **D**: Deposit.
- **b**: Bonus percentage.
- **W**: What you need to wager to clear the bonus.
- **RTP**: Return To Player (%). *Ex: RTP = 98%. Player plays 1000€. He can expect to get 980€ back.*
- **B**: Bonus amount.
- **n**: Wagering requirement. How much times I need to wager the bonus amount to clear it.
- **P**: Profit.
- **Volatility**: There can be a high deviation of RTP for small size samples.
- **G**: Gain constant, in percent.


## Concept
We can make money with online casinos with bonuses. The only requirement is to have a positive gain constant.
Here is the gain constant formula:
$$G = 1 - n(1-\frac{RTP}{100})$$

The gain constant tells us how much we can expect to earn, as it's a percentage of the bonus. If $G=0.2 (or\,20 \%)$, then I can expect to earn 20% of my bonus amount $B$. If it's negative, I can expect to loose.

To put the odds on our side, we have to target games with the highest RTP possible and the lower volatility.

## Proof
$$\begin{aligned}
B = b*D \\
W = B*n
\end{aligned}$$

In order to make a profit, we should in the end win more than the bonus amount. What we have to wager is W, what we will get back is $W*RTP$ (which is a percentage). What we keep is what we wager minus what we get back.

$$\begin{aligned}
W-\frac {RTP}{100}*W < B \\
1 - B/W < \frac{RTP}{100} \\
RTP > 100(1-\frac 1n)
\end{aligned}$$

We can now introduce a "gain constant" $G$. It represents the percentage of the bonus I'm winning (or losing). If the constant is positive, I'm winning money.
$$G = 1 - n(1-\frac{RTP}{100})$$

We can even calculate the profit:

$$
P = D*b*G
$$


## Example

I deposit 100$ and have a 100% bonus. The wager requirement is 40.

$$\begin{aligned}
RTP > 100(1-\frac 1{40}) \\
RTP > 97.5
\end{aligned}$$

I find a game with a 99% RTP.

$$\begin{aligned}
G = 1 - 40(1-\frac{99}{100}) \\
G = 0.6
\end{aligned}$$

I can calculate my expected profit.

$$\begin{aligned}
P = 100*1*0.6 \\
P = 60$
\end{aligned}$$

## Graphs

![Pasted image 20221219155021.png](/img/user/90%20Meta/Attachments/Pasted/Pasted%20image%2020221219155021.png)

![Pasted image 20221219155903.png](/img/user/90%20Meta/Attachments/Pasted/Pasted%20image%2020221219155903.png)



###### META
Status:: #wiki/notes/mature 
Plantations:: 
References:: 
