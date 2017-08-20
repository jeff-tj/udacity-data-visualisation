## Summary
I have chosen to work with my own dataset here and try to recreate charts that
I often use at work, but create with Excel. This would be a good example to try
and apply the skills that I have learned to a relevant area of interest.

In September this year, Australia will be entering its 26th year of growth 
without a recession (which is defined as 2 consecutive quarters of negative 
GDP growth). There are many theories that try to explain this, but a common one
is that the Reserve Bank of Australia (RBA - Australia's central bank) has
contributed to this by introducing an inflation target. I will attempt to allow
the reader to explore this theme in this visualisation by showing:
* RBA Cash Rate - the main tool the RBA has to influence the economy
* Inflation - the economic statistic the RBA is targeting
* Unemployment - another key statistic the RBA looks at
* GDP - the statistic used to determine whether there has been a recession

Please see below for further reading in the Resources Section

## Design
Initially the rough sketch I had done on a previous version in Excel had all
the data series represented as lines, however initial feedback from a colleague
pointed me to Chart 1 in Resource 2 - namely that it would be easier to see 
two consecutive quarters of negative growth if the GDP was represented as bars
(i.e. it would be easier for people to count 6 bars of negative growth and see
where we would be definied to be in a recession rather than having to guess it
from where the line crosses the x-axis).

Therefore, the chart was made with GDP as a bar chart and the rest the other
series as line charts.

At the same time, other colleagues commented that different people put differ-
ent weights on different data, so it would be helpful to allow the reader to 
toggle different series to suit their preferences.

A further design feature which I later added in myself was that I wished to 
create a "martini-glass" style chart, where I would lead the viewer through a
pre-defined narrative before allowing them to explore the data themselves. To
do this I added a column to define which regime (i.e. before the the RBA was 
targeting inflation - pre-1990s, or when the RBA was targeting inflation - 
post-1990, see Resource 1 for further information), I then toggled between the
regime hoping to show that before Inflation Targeting the economy was more 
volatile and experienced more recessions, while after inflation targeting the 
economy has continued more growing in a more stable manner.

## Feedback
Since I was trying to recreate charts that I often use at work, I showed my
ideas and charts to colleagues for feedback. This feedback is below (I could
not include the original emails due to work policy). Each is:
* "I think that you should display quarterly GDP as little columns. This makes it easier to see at a glance by counting the bars whether there was a recession or not. Have a look at a RBA discussion paper for how they presented it."
* "i couldnt care less about the GDP rate - all i want to see is cash, cpi and ue rate"
* "Overall the chart is a lot better than the Excel charts, but we know that the board wants the unemployment rate to decrease and not want it to increase. I think it is more intuitive if you could display the unemployment rate inverted." 
Unfortunately, despite spending much time on it, I was unable to find away to
have 3 different scales in dimple or have an inverted scale. Although this
could have been done in d3, I preferred dimple because of the built in feature
that displayed a pop-up with the series name and value - this allowed the
viewer to know the exact value of the datapoint they were interest in.

## Resources
### Resources used to understand data
1. Explanation of the RBA's policy: http://www.rba.gov.au/inflation/inflation-target.html
2. RBA Discussion on Growth: http://www.rba.gov.au/speeches/2010/sp-dg-200810.html
3. General News Discussion on Economy: http://www.abc.net.au/news/2016-09-07/gdp-australia-goes-25-years-without-recession/7823988

### Resources used for dimple construction
4. Example on toggling series: http://jsbin.com/sacaze/4/edit?html,js,output
5. Example on interactive legends: http://dimplejs.org/advanced_examples_viewer.html?id=advanced_interactive_legends
6. Another example on toggling series: http://jsbin.com/zadic/2/edit?js,output 

### Actual sources for the raw data
7. RBA cash rate, table F1.1 (RBA target rate, except IB rate jul-1990 and before): http://www.rba.gov.au/statistics/tables/#interest-rates
8. ABS Inflation data: http://www.abs.gov.au/ausstats/abs@.nsf/mf/6401.0
9. ABS Employment data: http://www.abs.gov.au/ausstats/abs@.nsf/mf/6202.0
10. ABS GDP data: http://www.abs.gov.au/ausstats/abs@.nsf/mf/5206.0