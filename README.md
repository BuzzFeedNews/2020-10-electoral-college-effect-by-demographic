# Analysis of Electoral College Effect By Demographic 

This repository contains the data and analysis for the BuzzFeed News article, "[The Electoral College Still Favors White Voters](https://www.buzzfeednews.com/article/johntemplon/the-electoral-college-still-favors-white-voters)," published Oct. 28, 2020. It is an updated version of [the analysis that BuzzFeed News ran in November of 2016](https://github.com/BuzzFeedNews/2016-11-voter-power-by-demographic).

## Data

The data for this analysis came from two sources:

- __The U.S. Census__. The [`data/census`](data/census) contains three files: `Table 4b` from the Census's [Voting and Registration in the Election of November 2016](https://www.census.gov/data/tables/time-series/demo/voting-and-registration/p20-580.html), a slice of the Census's Current Population Survey, which was obtained through the [CPS Table Creator](http://www.census.gov/cps/data/cpstablecreator.html), and the 2019 American Community Survey's demographics for Maine and Nebraska's congressional districts (see the note about Maine and Nebraska below).

- __FiveThirtyEight__. This analysis uses FiveThirtyEight's "Voter Power Index" from their [2020 Election Forecasts](https://github.com/fivethirtyeight/data/tree/master/election-forecasts-2020). BuzzFeed News downloaded the data on October 28, 2020 at 10 am; you can find it in the [`data/fivethirtyeight`](data/fivethirtyeight) directory.

## Analysis

The full analysis [can be found here](notebooks/analysis.ipynb). It uses the Voter Power Index and 2016 voter registration data to quantify relative voting power vis-a-vis race.

### Note on Maine and Nebraska

Maine and Nebraska partly assign their electoral college votes by Congressional district. `Table 4b` of the Census data described above does not provide registered voter counts by demographic for individual districts. So, in order to estimate those numbers, BuzzFeed News used the Census’ 2019 estimates of voting-age citizens by demographic group in each district, and then reduced those counts in proportion to the ratio of registered voters to voting-age citizens in each state. This represents an improvement over BuzzFeed News’ 2016 analysis, which did not analyze Maine and Nebraska’s district-level votes. But given the relatively small number of people living in these districts, the few electoral college votes they represent, and the range of VPI estimates for the districts, this change has a negligible effect on the overall results.

## Questions / Comments?

Please contact John Templon at john.templon@buzzfeed.com.

Looking for more from BuzzFeed News? [Click here for a list of our open-sourced projects, data, and code](https://github.com/BuzzFeedNews/everything).
