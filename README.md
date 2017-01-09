Summary - This dataset is from the peer-to-peer lending platform Prosper and includes information on both those using the platform to
lend and to borrow.  The set has been paired down to 16 variables on borrowers only. The chart is specifically looking at the relationship of the lender's return on investment vs. the borrower's rate charged.



Design - My goals with this visualization is to show the reader the relationship between the lender's return on investment (ROI) vs the
borrower's lending rate.  I also show how the borrower's Prosper Rating affects the lender's ROI by aggregating the data on those categories.  I initially show a scatter plot of a sample set of the entire data to give the reader an idea of how borrower interest rate and Prosper Rating affect the lender's return.  Then I performed some data analysis in R to calculate the mean ROI and borrower rate for each Prosper Rating group to more clearly ilucidate the above described trend.  For both of these plots I encoded the Prosper Rating in color to easily distinguish between groups and to illustrate the effect of Propser Rating on ROI.  My last plot is a bar plot of the ROI variance which shows how the risk increases with lower Prosper Rating.



Feedback - After creating my initial scatterplot, I discovered that what I wanted to render was too large for a browser.  So, I
decided to pursue a slightly new direction with my visualization goal.  Rather than render every data point on the EstimatedReturn vs.
BorrowerRate plot, I used R to group the samples by ProsperRating..Alpha. and took the mean of each group.  This shows a clear
proportional relationship.  I may go back and lead the reader with a sub-sampled scatter plot of the original graph as well.  The
feedback was provided in the following forum discussion.
https://discussions.udacity.com/t/final-project-dimple-scatter-plot-help/204856



After my second attempt at making the three plots, I showed them to my wife and she said that I should add context to the graphs.  So, I added descriptive paragraphs before each plot.  These paragraphs help to explain the findings in the data.  These updates were incorporated in the second index.html file.

Next, I posted my visualization on the Udacity forum below.  
https://discussions.udacity.com/t/visualization-final-project-feedback/206862/3
In response, I added a legend for the Prosper Rating color scheme and I also increased the size of the circles.  I didn't lose the gridlines afterwards because I think they do maintain a frame of reference that's easy for the reader to interpret.  I also didn't use different shapes because I felt that it could slow down interpretation due to multiple encodings.  I included these changes in the third index.html file.


Lastly, I added a more sophisticated interaction.  After researching how to add a legend, I found another example that showed how to filter the data on a click event in the legend.  These changes were implemented in the final index.html file.

Resources -
https://discussions.udacity.com/t/how-to-scale-data-values-in-dimple-js/203187
http://stackoverflow.com/questions/23301738/dimple-x-y-chart-without-aggregation
https://discussions.udacity.com/t/p6-sharing-how-to-make-a-gist/43772/17