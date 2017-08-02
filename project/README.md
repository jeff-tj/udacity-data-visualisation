## Introduction
Since it has been relevant to my work I have been working with a lot of data
with regards to Australian economic data and its effect on the Reserve Bank
of Australia's (RBA) decision making process in setting interest rates. The bulk of
this has been using Excel. Therefore I have decided to try and recreate similar
charts using d3 and dimple, to get feedback as to how these charts are better
than standard Excel charts.

The time period observed is from 1990 onwards, this is crucial as this is the
time where the RBA switched to an inflation targetting framework. Since then
Australia has managed to go the longest period of time without a recession.

I try to tell this story in my chart.

Further reading available here:
http://www.abc.net.au/news/2016-09-07/gdp-australia-goes-25-years-without-recession/7823988
http://www.rba.gov.au/speeches/2010/sp-dg-200810.html
http://www.rba.gov.au/inflation/inflation-target.html

## The Data Fields
The data fields that most people consider relevant are:
* cash_rate - the main interest rate that the Reserve Bank of Australia sets, 
this has an effect on all other interest rates in the economy
* cpi - the main measure of inflation in Australia. Note - the data is only
produced quarterly, so for months without data take the previous release
* gdp - Gross Domestic Product is the main measure of economic growth in 
Australia, the data is only produced quarterly, so for months without data take
the previous release
* ue - Unemployment Rate is the main measure used to gauge the quality of the 
labour market in Australia, here I have provided both a national number as well
as a state by state number

## Selecting Colors
We use color brewer to select an scheme of colors, relying mainly on pastel
colors to improve readability.
http://colorbrewer2.org/
*Grey Bars: #bababa
*Cash Rate: #d7191c
*Inflation: #abd9e9
*u/e: #abdda4
Note we since we want to focus on the cash rate, we make this a solid color.
For the rest we use softer pastel shades, as well as reduce the opacity.