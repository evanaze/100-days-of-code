# 100 Days Of Code - Log

### Day 1: Monday, January 04, 2021

**Today's Progress**: I found one simple error, having `head()` unneccessarily which was cutting my results into just 5.
Unfortunately, this revealed that my previous bug has not been fixed as I had thought.
I wanted to start work on the test object and run my first backtest, but it looks like I am stuck until I figure out this really strange bug.

**Thoughts**   
This bug is super frustrating and I can't find anything about it online. I also can't reproduce it on a jupyter notebook. Maybe I should make sure the environments are the same.
It's frustrating that we know there are not any duplicate indicies, which would be the usual reason for a `IndexValueError`.

**Link(s) to work**
N/A so far.

### Day 2: Tuesday, January 05, 2021

**Today's Progress**: Slammed my head against the wall for a bit about the bug. That's it.

**Thoughts**   
I am glad I put in the work today, even though nothing came of it.

**Link(s) to work**
N/A so far.

### Day 3: Wednesday, January 06, 2021

**Today's Progress**: Fixed the damn bug. Also, wrote the script for a test, so now we can start doing back tests of real life strategies **!**.

**Thoughts**   
It feels good to be a gangster. Can't wait for that sweet, sweet easy dough to be coming in.

**Link(s) to work**
N/A so far.

### Day 4: Thursday, January 07, 2021

**Today's Progress**: Separated the `Preprocessor` object into two files. I am hoping this makes it easier for me to create pairs data for backtesting, but I have not wrapped my mind around that yet.
Also, Amberdata announced that they added new exchanges to their API, so I can put off moving to cryptochassis for a while longer.
I also investigated why I could not access my EC2 instance. Remains to be seen why that is the case.

**Thoughts**   
I don't think I made much of any real progress by moving my code around like that. I wish I knew if there were actual guidelines about how best to do this.

**Link(s) to work**
N/A so far.

### Day 5: Friday, January 08, 2021

**Today's Progress**: Created raw pairs trades data. Also started my first Twitch stream.

**Thoughts**   
I will probably want to do dynamic bars next, because I am not sure how to group the pairs data into bars.

**Link(s) to work**
N/A so far.

### Day 6: Saturday, January 09, 2021

**Today's Progress**: Refactored the backtest library a bit, worked on dynamically grouping trades into bars.

**Thoughts**   
It took longer than I would have thought, and the code base is messier than I would anticipate.

**Link(s) to work**

### Day 7: Sunday, January 10, 2021

**Today's Progress**: Grouped trades by dynamic bars sizes.

**Thoughts**   
Next time I should:
* Look into the statistical properties of the bars I made, and make sure that there aren't any anomolies.
* Think about making the dynamic grouping into a Kalman Filter.

### Day 8: Monday, January 10, 2021

**Today's Progress**: Implemented strategy and finished grouping trades into bars.

**Thoughts** 
Not sure how long to make the back looking returns variable. Currently it is set to 1 hr, but the time barrier is set to 15 minutes.
Should we be calculating returns on a minute by minute basis?

Should we be using VWAP? Might be best for a momentum based strategy.

### Day 9: Wednesday, January 12, 2021

**Today's Progress**: Learned about Fractional Differentiation, and did some EDA on my tick bars.

**Thoughts** 
I should review the general workflow for building a strategy, and whether I should test the naive model before I work on the Meta Model.
How many times should I try to trade in a day?

### Day 10: Thursday, January 13, 2021

**Today's Progress**: Plotted Boll bands on the pairs data, I think we are good to go with labeling trades next. Afterwards, time to train an ML model.

**Thoughts** 
Ratio is fine for coint.
No need to re-scale data.
If we start writing too many bars, then the boll bands will change too rapidly in the given setup. May want to make boll bands based on time instead of bars. On second though, scratch that.
