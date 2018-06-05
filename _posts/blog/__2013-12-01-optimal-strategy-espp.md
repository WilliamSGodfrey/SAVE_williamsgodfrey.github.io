---
id: 681
title: 'ESPP - Optimal Strategy for Employee Stock Purchase Plans'
date: 2013-12-01T17:57:58+00:00
layout: post
guid: http://www.williamsgodfrey.com/?p=681
permalink: /optimal-strategy-espp/
dsq_thread_id:
  - 2021373408
categories:
  - Personal Finance
excerpt: "A short post discussing a my interpretation of the ideal strategy one should use when participating in an Employee Stock Purchase Plan."
comments: true
share: true
---
A friend, &#8220;Tim&#8221;, recently asked for my guidance related to his participation in his employer provided employee stock purchase plan (ESPP). ESPPs are a form of additional compensation offered by some companies that allow employees to purchase stock in the company they work for at a discount. The specific terms of each ESPP out there are slightly different, but the general idea is that employees contribute to the plan through payroll deductions, which build up between the offering date and the purchase date. At the purchase date, the funds are used to purchase shares in the company on behalf of the participating employees at a discount.

Tim specifically wanted to know 3 things. First, did I think he should be participating in the ESPP? Then, if yes, how much should he be contributing? And then finally, should he sell or hold the stock after the purchase date (and how long should he hold)?

I think the genesis of these questions is based partly in naiveté about tax law and financial planning but also in the uncertainty of quantifying the opportunity cost and difficulty in calculating the return on investment (ROI) of such an opportunity.

[This is a long, post full of good stuff, but if you're in a hurry to see my answer to Tim's questions, [jump to the summary](#Summary).]

## The ESPP Details

All ESPPs are a little different and I needed the full picture to answer those questions. The ESPP available to Tim has a 6 month accumulation period, maximum contribution rate of 10%, no required holding period, and a 15% discount on the stock price at market closing on purchase day.

If you're unfamiliar with ESPPs that might not be entirely clear. It means that a specified amount of money will be deducted from each of Tim's paychecks, up to a maximum of 10% of his gross pay, over the course of a six month period. At the end of those six months, stock will be purchased using the money that has been deducted. The stock is purchased at a price that is 15% lower than the price of the stock on purchase day. For example, if the stock is $10 at market closing on purchase day, the purchase price would be $10.00 - (0.15 x $10.00) = **$8.50**. Quite the deal, huh?

It initially seemed pretty straight forward to me. Tim should contribute the maximum amount to the ESPP and he should sell the stock immediately. This guarantees an ROI of at least 15% with virtually no risk. The most difficult part of this exercise is proving that quantitatively.

## Opportunity Cost

The first step is going to be calculating the [opportunity cost](http://en.wikipedia.org/wiki/Opportunity_cost)of participating in the ESPP. I'll assume that Tim is paid twice a month and be extremely generous and assume that Tim can receive an annualized ROI of 10%. Now we can do a bit of calculation:



You'll notice that I've calculated the [internal rate of return](http://en.wikipedia.org/wiki/Internal_rate_of_return) (IRR) as well as the ROI. I did this because I felt that ROI was a poor indicator for this analysis. ROI is a simple calculation that does not consider the periodic nature of the contributions in this analysis. It only considers the final investment gain and the original investment amount. IRR, on the other hand, is the &#8220;annualized effective compounded return rate&#8221; and incorporates, among other things, the time each dollar is tied up in an investment. The choice to use IRR may not be as clear here, but will become more clear when we quantify the potential return of Tim's participation in the ESPP in the next section. IRR is also fairly widely used in financial applications to compare various investment opportunities, which is exactly what we're doing here.

So we see from above that Tim could realize an IRR of 21.71% if he invested his money instead of contributing it to the ESPP. At first glance, this seems _higher_ than expected. Let's see how that compares to the IRR for the ESPP.

## Investment Return via ESPP

The reasons behind using IRR become most obvious here. It is quite difficult to determine the potential return from participation in an ESPP when one considers the accumulation period and periodic nature of the paycheck deductions. As soon as the money is deducted from Tim's paycheck and held, we should consider it &#8220;invested.&#8221; It is unavailable for him to use elsewhere. Therefore, the dollars that are deducted from Tim's paychecks towards the beginning of the accumulation period will have a lower effective return that the dollars that are deducted from Tim's paycheck towards the end of the accumulation period. Those early dollars will return the same absolute amount as the later dollars, but they'll do it over a longer time period. This is where IRR excels:



So there we have it. It's pretty clear that, ignoring tax implications, the return on participating in the ESPP far exceeds the return Tim could find elsewhere during the same time period.

## ESPP Tax Implications and Optimization

The whole story isn't really complete until we consider the taxes that Tim is going to need to pay on the money he might make by participating in the ESPP.

The tax rules concerning ESPPs are fairly straightforward. If Tim sells his shares within 1 1/2 years of purchasing them, they are taxed as income. For this analysis I used his highest marginal tax bracket, in Tim's case this is 28%. This changes the IRR calculation a bit:



As we concluded above, Tim's participation in the ESPP and selling the stock immediately remains the better strategy, even when we consider the tax implications. His IRR just falls a tad to 54.18%.

However, this isn't necessarily the optimal strategy in terms of maximizing return (by minimizing tax exposure). If Tim were to hold the stock for 1 1/2 years after his purchase date, his gains would be taxed at the Long Term Capital Gains tax rate, which is only 15% (in 2013). Of course this also exposes Tim to a degree of risk. In the previous analysis, Tim was completely sheltered from any risk related to market volatility since he was selling the stock the instant he purchased it.

If Tim is willing to take on the extra risk, he'll realize a slightly higher IRR:



By setting up a system in which he holds stock for 1 1/2 years, his effective IRR[^1], once he eventually starts selling the stock, will be the highest out of all the scenarios considered here.

[If you'd like to get your hands on the worksheets I put together to perform this analysis, take a look here: <a title="ESPP Analysis" href="https://docs.google.com/spreadsheet/ccc?key=0Aiu4oxRTFijmdHdGUUZCNmV1dnc4T05NX2xzODZIcFE&usp=sharing">ESPP Analysis</a>]

##<a name="Summary">Summary

So what did I tell Tim?

Tim should participate in his ESPP. It will provide a better return than any other financial instrument he is likely to find elsewhere. He should contribute the maximum amount possible and, if he is comfortable with the risks inherent in holding market securities, should sell them after holding them for 1 1/2 years to optimize his tax liability. However, I recommended that Tim sell the stock immediately, despite the higher tax hit, in order to minimize his risk exposure to his company. He already relies on his company to pay his wage, I didn't see much sense in further tying his financial success to the company performance. If the company were to suddenly disappear one day, Tim would be out of a job _as well as_ out whatever money he had invested in the company.

Things to keep in mind here are that the details of each ESPP will be different and this advice isn't &#8220;one size fits all .&#8221; Some ESPPs will dictate a required holding period, or a transaction fee, or whatever that should all be taken into account before choosing whether and to what degree to participate.

  
---

[^1]: I'm calculating an effective IRR here. Once Tim has his system up and running and he's cycling through stock, he'll be selling stock on the purchase days. The stock he's selling will just be two years old. One could argue that we can ignore any price movement that might be happening during Tim's 1 1/2 year holding period since he is effectively selling the stock as soon as he buys if (with the exception of 3 lots). Doing this allowed me to _greatly_ simplify the calculation of the last IRR since I didn't need to determine the likely behavior of that stock.
