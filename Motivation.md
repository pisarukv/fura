Problem
===================

In one point appeared an idea to try analyse working repositories to get data on working efficienty and different metrics. Then we decided to find tools that could collect data on repo and give it to use.  
But most of this tools were applications with fixed reports. Using this data for building other metrircs wasn't possible.

GitStats and GitInspector was the main apps that were fund. Although they worked relatively quickly, they had very large disadvantages and were not suitable for our purposes.

https://github.com/ejwa/gitinspector

http://gitstats.sourceforge.net/

# GitInspector

First we tried to use GitInspector. He worked fast but had a lot of downsides. When we tried to analyse go repo we found out that GitInspector works with not all programming languages . Also it skips a lot of commmits. It were losing from 30% to 60% commits. Also data generated but this tools was impossible to use for building other statistics. 

# GitStats

After that we tried to use GitStats. It was slower than GitInpsectora but still fast enough. Also he didnt skip commits and could analyse all programming languages. Also statistics was more detailed but still it was accumulated and wasnt enougth to build different metrics.  Other problems was that it made analysis only of the current branch and it didnt distinguish programming languages text from other text. For example it would count automatically generated json as lines of code.

# Fura

Because of all of this we decided to create our own tool that we could use for collecting date for futher experements. As a programming language we decided to use go. It is easy to launch on any platrofm and binary file is lightweight. 
We called it fura

App returns data as a json of writed the to mongoDB. It allows to use it both as a microservice as well as ussual app. 

# Data format

Data fura returns is in `json` format. To see the structure you can visit [wiki page](https://github.com/cali4888/fura/wiki/Data-format)

Becose of this inforamtion that is given by our app suited our need to makes different statistics on repos.  

# Comparing

We made some tables to compare our tool to previosly metioned tools.

Posgtress repo table 
https://github.com/postgres/postgres

| **Name** | **Commits number**| **Time** | **Added Lines** | **Removed Lines** |
|------|---------|------|-----|------|
| Github | 43462  | |||
| Git cmd | 59947  ||||
| Fura  | 52735 |31m18s| 4506783 | 3402561 |
| GitInspector |  26341 | 20m|3259353|1909316|
| Gitstats | 43425 |33m 42s| 10107314 | 7127229 |


React repo table 
https://github.com/facebook/react

| **Name** | **Commits number**| **Time** | **Added Lines** | **Removed Lines** |
|------|---------|------|-----|------|
| Github | 9020  | |||
| Git cmd | 12769  ||||
| Fura  | 10642 |5m33s| 1485310 | 1182386 |
| GitInspector |3351 |30s|487370|393511|
| Gitstats | 9006 |3m 32| 884361 | 670862 |

As you can see on smaller repos our app a bit looses to gitstats and strongly gitInspector. But last one ignores a lot of commits. As for bigger repo fura works faster than gitstats. Also the number of commits is larger that other tools. It is becose gitInspector skips a lot of commits and gitstats analyses only the current branch.  Also there is large difference in number of lines becose other tools cound as lines a lot of authogenerated content. 

In the end we were able to create a comfortable tool to analyzing git repos which can be used to  calculate different statistics which is not inferior in time or stability to other existing tools. 
