# Reward-Enhanced-Point-Refund-Policy-for-Consumer-Retention-in-E-Commerce
A supply chain modeling project that investigates reward-enhanced point refund policies as a strategy for consumer retention in e-commerce

## Background

After the COVID-19 pandemic, contactless consumption has rapidly expanded, leading to significant growth in the e-commerce market. Over the past five years, the total volume of online shopping transactions has increased by approximately 1.6 times, and consumer purchasing behavior has shifted from offline-centered shopping to online platforms.

Online shopping provides consumers with convenience, accessibility, and a wide variety of product options. However, because consumers cannot physically inspect products before purchasing, the number of product dissatisfaction cases and return requests has increased.

In Korea, the annual number of parcel return shipments exceeds 500 million, accounting for roughly 10% of total deliveries.

Moreover, negative experiences during the return process can reduce customer satisfaction and lead to customer churn. To mitigate this issue, companies often adopt lock-in strategies to retain customers.

In this project, we perform a **supply chain modeling analysis** to investigate whether adopting a point-based refund policy, rather than a conventional cash refund policy, can reduce customer churn and improve firm profitability.

## Problem Definition

In conventional refund policies, customers often terminate their relationship with the brand after receiving a cash refund. This increases the likelihood of customer churn.

To address this issue, this study proposes a **Reward-Enhanced Point Refund Policy**.

  - Provide refunds in reward points instead of cash
  - Offer a higher value of points than the equivalent cash refund

This policy is expected to create the following effects.

[Consumer perspective]

  - Consumers receive a higher perceived reward compared to a cash refund.
  
[Manufacturer perspective]

  - Encourage repurchase through point usage

  - Improve long-term customer retention

In practice, similar strategies have been implemented in the airline industry. For example, several airlines have offered 10–20% additional credits when customers choose vouchers instead of cash refunds.

## Modeling

$D = d_0 - d_1 p + d_2 r - \mathbb{I}[r = r_{point}] \cdot d_3 (r_{exp} - r)$

$E = e_0 + e_1 r - \mathbb{I}[r = r_{point}] \cdot e_2 (r_{exp} - r)$

$\Pi = pD - rE + \mathbb{I}[r = r_{point}] \cdot pE$

  - $p$ : product price
  - $r$ : refund amount
  - $r_{exp}$ : consumer's expected refund amount

  - Conditions
      - $d_1 > d_2 > d_3$
      - $e_1 > e_2$
      - $e_1 > d_2$
      - $e_2 > d_3$
      - $d_i, e_j > 0$
      - $D > E$
      - Consumers prefer cash refunds to point refunds
      - Consumers have no dissatisfaction with the cash refund amount 
      - Consumers expect a full refund : $r_{exp} = p$
   
If  $p = \frac{2 d_0 e_1 - d_2 e_0}{4 d_1 e_1 - d_2^2}$, $\Pi_{point} - \Pi_{cash} > 0$
