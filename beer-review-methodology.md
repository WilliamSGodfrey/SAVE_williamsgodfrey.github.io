---
id: 373
title: Beer Review Methodology
date: 2013-10-27T18:36:34+00:00
layout: page
guid: http://www.williamsgodfrey.com/?page_id=373
dsq_thread_id:
  - 2024312429
---
With each beer review I try to judge the beer based only on beers of its same style. Sometimes that is very difficult (<a title="not very many (any?) similar beers" href="http://www.williamsgodfrey.com/kvasir-dogfish-head/" target="_blank">Kvasir</a>, for example).

If one goes back and looks at all my ratings you can probably see which beer styles I like the best and which I like the least. I try to only review beer styles that appeal to me to counteract this bias.

#### Numerical Ratings

Each beer review is comprised of 5 numerical scores that are based on the 5 characteristics listed below. Each numerical scores ranges from 1 to 5. I include a brief description is each review category as well.

  * **appearance** = 5%, <span style="line-height: 1.5em;">I note the beer&#8217;s color, carbonation, head and its retention.</span>

  * **smell** = 20%, <span style="line-height: 1.5em;">I note the beer&#8217;s aromatic qualities.</span>

  * **taste** = 45%, <span style="line-height: 1.5em;">I take a deep sip of the beer and note any flavors, or interpretations of flavors.</span>

  * **mouthfeel** = 10%, <span style="line-height: 1.5em;">I note how the beer feels on the palate.</span>

  * **overall** = 20%, <span style="line-height: 1.5em;">My overall impression of the beer.</span>

At the end of the review I calculate the beer&#8217;s Final Rating by taking a weighted average of the numerical scores from each characteristic using the percentages indicated above. This gives a nice idea of the quality of the beer. It doesn&#8217;t really take into account the economy of the beer though.

### aFR

There is a huge variety of really good beer out there. The &#8220;craft beer revival&#8221; that the US has experienced in the last 20 years, even in just the last 5 years, has resulted in a wide disparity between beers with respect to price and container volume. It is quite difficult to decide whether a great beer is &#8220;worth&#8221; its great big price tag. Everyone will have their own subjective opinion on whether Beer A is a better deal at price X than Beer B is at price Y, but my &#8220;aFR&#8221; or **a**djusted **F**inal **R**ating (What can I say? I took a very literal approach to devising my acronym.) is my attempt to standardize beer ratings.

I calculate _aFR_ as follows:

$$
\begin{align*}
  aFR = \frac{Final_Rating}{\frac{Price}{Volume}} + sign(\beta)*\beta^2
\end{align*}
$$

where:

 $$ \beta $$ = $$ \frac{X-E[x]}{\sigma(x)} $$  
 $$ \sigma(x) $$ = $$ \sqrt{Var(x)} $$  
 $$ x $$ = The set of all Final Ratings

 See Wikipedia for [more information](http://en.wikipedia.org/wiki/Standard_score#Standardizing_in_mathematical_statistics).

&nbsp;

This will result in a number that should make it a little clearer as to the relationship of a beer&#8217;s quality and price. My idea is that the _aFR_ will tell one how &#8220;efficient&#8221; the beer is; how many Points you are buying with each Dollar (while also considering how much volume of that beer you&#8217;re getting). The _aFR_ will increase as the Final Rating increases but it will decrease if the price increases _without also increasing the quality above the average of all beers reviewed_.  In theory this will help me decide if that Revolution Brewing Deth&#8217;s Tar at $15 will provide me a better bang for my dollar than the Toppling Goliath Brewing Kentucky Brunch Brand Stout at $22.

The trickiest (most valuable?) part of this rating system is that it is relative to all other beers reviewed. That means that as I review more beers and compile more data, the _aFR_ of beers that I have already reviewed will change depending on how the new reviews affect the value of the average of all the Final Ratings. This is why the _aFR_ on each beer review page is a dynamic field that will update every time I add a new beer to my database.

This system is clearly not perfect. The _aFR_ is already on its second iteration. I&#8217;m always open to suggestions on how I might be able to better capture this idea mathematically.

&nbsp;

For a list of all the beers I have reviewed (and their scores) check out the <a href="http://www.williamsgodfrey.com/summary-beers-reviewed-scores/" target="_blank">Summary of Beers Reviewed and Scores</a> page.