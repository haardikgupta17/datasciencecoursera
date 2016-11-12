# How to share data with a statistician
This is a guide for anyone who needs to share data with a statistician or data scientist. The target audiences I have in mind are:<br/>
* Collaborators who need statisticians or data scientists to analyze data for them<br/>
* Students or postdocs in various disciplines looking for consulting advice<br/>
* Junior statistics students whose job it is to collate/clean/wrangle data sets<br/>

The goals of this guide are to provide some instruction on the best way to share data to avoid the most common pitfalls and sources of delay in the transition from data collection to data analysis. The [Leek group](http://jtleek.com) works with a large number of collaborators and the number one source of variation in the speed to results is the status of the data when they arrive at the Leek group. Based on my conversations with other statisticians this is true nearly universally.<br/>

My strong feeling is that statisticians should be able to handle the data in whatever state they arrive. It is important to see the raw data, understand the steps in the processing pipeline, and be able to incorporate hidden sources of variability in one's data analysis. On the other hand, for many data types, the processing steps are well documented and standardized. So the work of converting the data from raw form to directly analyzable form can be performed before calling on a statistician. This can dramatically speed the turnaround time, since the statistician doesn't have to work through all the pre-processing steps first.
## What you should deliver to the statistician
To facilitate the most efficient and timely analysis this is the information you should pass to a statistician:
1. The raw data<br/>
2. A [tidy data set](http://vita.had.co.nz/papers/tidy-data.pdf)<br/>
3. A code book describing each variable and its values in the tidy data set.<br/>
4. An explicit and exact recipe you used to go from 1 -> 2,3<br/>
Let's look at each part of the data package you will transfer.
### The raw data
It is critical that you include the rawest form of the data that you have access to. This ensures that data provenance can be maintained throughout the workflow. Here are some examples of the raw form of data:
* The strange [binary file](https://en.wikipedia.org/wiki/Binary_file) your measurement machine spits out<br/>
* The unformatted Excel file with 10 worksheets the company you contracted with sent you<br/>
* The complicated [JSON](https://en.wikipedia.org/wiki/JSON) data you got from scraping the [Twitter API](https://twitter.com/twitterapi)<br/>
* The hand-entered numbers you collected looking through a microscope<br/>
You know the raw data are in the right format if you:
1. Ran no software on the data<br/>
2. Did not modify any of the data values<br/>
3. You did not remove any data from the data set<br/>
4. You did not summarize the data in any way<br/>
If you made any modifications of the raw data it is not the raw form of the data. Reporting modified data as raw data is a very common way to slow down the analysis process, since the analyst will often have to do a forensic study of your data to figure out why the raw data looks weird. (Also imagine what would happen if new data arrived?)
