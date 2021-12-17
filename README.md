
# Political Differences on Main Political Subjects in US Congress

[URL to the datastory](https://medium.com/@badrlarhdir7/political-differentiations-on-main-political-subjects-in-us-congress-87495667c171)

### Abstract
Gun policy, immigration, and climate change are examples of subjects for debate that tend to divide lawmakers. Throughout this data story, the goal is to analyze to what extent there is an ideological split in the quotes related by Quotebank between the two political parties. Note that only the quotes of politicians that were part of Congress from 2016 to 2020 were selected.

### Research questions
To what extent do republicans and democrats' opinions differentiate on immigration, climate change, gun policy and healthcare ? 

### Additional datasets
We used as a dataset the quotes of elected congressmen between 2016 and 2020. Indeed by selecting elected members we have an objective criteria that defines the political affiliation to the speaker of a quote.

Also, all congressmen that were not reelected in the midterm 2018 elections or that quitted their position are removed from the dataset. Indeed we want to make sure that each elected official has the same timeframe.

On top of that, we decided to remove the president and vice president from the dataset. Indeed, news outlets would tend to give more speech time to the president of a nation regardless of his political affiliation. And this would bias the result as the party of the president would be over-represented.

Note that we did not take the political parties from the data provided in speaker_attributes as we saw it was incomplete. Also, we planned to only keep the parties Democrat and Republican as the Independent party only contains one politician from 2016 to 2020.

### Methods
In order to determine if democrats and republicans have different opinions on the chosen topics we used the following methods that have proven to be successful and others that have not:

##### Method 1: Document classification<br/>
This analysis allows us to address the question: Can we detect quotes from a specific party (e.g. either democrats or republicans) among all quotes on a selected topic? A regularized logistic regression is fitted on labeled quotes (democrat or republican speaker) used for training. In order to address the issue of high dimensionality, we used crossvalidation on the regularization parameter on the training set. The resulting accuracy informs us if we can perfectly predict paragraphs from democrats or republicans. Additionally, from the model built, the words characterizing the party to be detected are retrieved and allow for further interpretations and comparisons between parties. This method has proven to be successful regarding the accuracy obtained.


##### Method 2: Sentimental analysis<br/>
For every topic, the sentiment scores of the quotes are retrieved using VADER sentiment analysis tools. The score obtained ranging from -1 (most extreme negative) and +1 (most extreme positive) are used to select solely the positive (score >0.5), negative (score < -0.5) and ignore the quotes labeled as neutral. In a second step, the share of positive (respectively negative) quotes stated by either democrats or republicans are analyzed in order to verify whether the obtained results are consistent with the known initial views of the parties. This method has proven to be unsuccessful as we concluded that sentiments are not representative of the opinion conveyed by democrat or republicans


### Organization within the team
To begin with, all four members formulated the problem and the research question. We also  jointly performed various analyses during the third milestone on the four topics. Finally we investigated together whether the obtained results are conclusive and which one are kept for the datastory.

Ahmed: Initial observation studies, topic detection algorithm formulation, writing up the datastory<br/>
Badr: Initial dataset filtering, code structuration, preparing the datastory on the website<br/>
Félicia: Preliminary data analysis for each topic, running tests with sentimental analysis, writing up the datastory<br/>
Nina: Preliminary visualisation, running tests with sentimental analysis<br/>
 

### File descriptions on git
<ul>
  <li> <em>analysis_complete.pynb</em>: Single notebook supporting all required analyses to investigate the research question including data loading, analyses (document classification and sentiment analyses) and production of plots for the datastory
    
