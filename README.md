## Defund the Police?

After the horrific murder of George Floyd on May 25, 2020 Americans nationwide marched to protest the decades-long mistreatment of African Americans by law enforcement officers. From this movement came a reasonablely large call to "Defund the Police", which implored city governemnts to move some amount of funds away from their police dpartments and toward community resources like "social services, youth services, housing, education, and healthcare" (Wikipedia). This made me ask the question...

## ...is there a coorelation between police spending and crime rate?

First I had to gather data. 

I found a .csv listing rates of homicide, rape, robbery and aggravated assault rates for 69 cities over 40 years. This file was from The Marshall Project, a "nonprofit, online journalism organization focusing on issues related to criminal justice in the United States" (themarshallproject.org). From this data, I was able to derive a unique "crime rate" metric for every city and every year; adding up the totals of the four above crimes, dividing by population, and multiplying by 100,000. This calculation was taken from the California Attourney General's Office website. 

I also had to gather city government spending data, and was able to do so through The Lincoln Institute of Land Policy, a Cambridge, MA thinktank that "seeks to improve quality of life through the effective use ... of land" (lincolninst.edu). The file included numbers on how much a city spent on welfare, corrections (jail), and police, and I was able to get data for 53 cities over 38 years

I merged the two files into one Pandas DataFrame, so I could easily navigate through the data. 

## Exploratory Data Analysis

Out of curiosity, I wanted to see which cities had consistently high crime rates from 1975 to 2015, the time-span of the data set. I did so by ranking the top 50 annual crime rates and seeing which cities showed up most in that ranking. The graph illistrating that is below. 







I also wanted to do the same for police spending, corrections spending, and welfare spending. Those three graphs are below.







## Statistical Tests

*Welfare vs Crime*

*Null Hypothesis (Ho): there is no correlation between welfare spending and crime rate*
*Alternative Hypothesis (Ha): there is a correlation between welfare spending and crime rate*

First, I wanted to find the coorelation between welfare spending and crime rate. I ran a t-test and Mann Whitney Test but because half the welfare data were unusable, the numbers were wildly inconsistent. I was not able to make a call whether or not to reject my null hypothesis. 






As expected, the graph trying to visualize this coorelation is unusable, since a lot of the blue data points are zero. The graph is very inconsistent and jagged. 






*Corrections vs Crime*

*Null Hypothesis (Ho): there is no correlation between corrections spending and crime rate*
*Alternative Hypothesis (Ha): there is a correlation between corrections spending and crime rate*

Next, I wanted to find the coorelation between corrections spending and crime rate. I ran a t-test and Mann Whitney Test but because half the welfare data were unusable, the numbers were wildly inconsistent. I was not able to make a call whether or not to reject my null hypothesis. 






As expected, the graph trying to visualize this coorelation is unusable, since a lot of the gray data points are zero. This graph is very inconsistent and jagged as well.






*Police vs Crime*

*Null Hypothesis (Ho): there is no correlation between police spending and crime rate*
*Alternative Hypothesis (Ha): there is a correlation between police spending and crime rate*

Finally and most of all, I wanted to find the coorelation between police spending and crime rate. I ran a t-test and Mann Whitney Test, and becuase I had lots of valid data, I was able to draw a conclusion. I was able to reject my null hypothesis.






The graph trying to visualize this coorelation makes perfect sense. As median police spending rises, median crime rate falls. 

## Conclusion

The notion that there's a coorelation between police spending and crime can't be ruled out. Both our police system as well as our unconsious biasses need lots of work, but the idea of "defunding the police" might need some more work before is it put into practice.
