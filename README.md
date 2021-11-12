# Political Differentiations on Main Political Subjects in US Congress

### Abstract
To what extent do politicians' opinions differentiate on major issues? Gun policy, illegal immigration, abortion and climate change are examples of subjects for debate that tend to divide lawmakers. It appears interesting to analyse to what extent there is an ideological split between different parties (Republican, Democrats), that is identifiable in quotes of politicians. Throughout this journey, it is planned to explore three to four themes, depending on the conclusivity of our results. The subjectivity of quotes will be analysed per party and in addition, a quantitative analysis will be done to present interesting facts on the chosen themes.

### Research questions
Are Democrats or Republicans personalities associated with positive or negative vocabulary/emotions about one policy such as gun policy, illegal immigration, abortion and climate change?
Which major attributes of politicians can explain his/her opinion on a precise issue? 
How do quotes about one issue evolve throughout the years, from 2016 to 2020? Which other facts are interesting to present about these subjects?


### Additional datasets
We will use as a dataset the quotes of elected congressmen between 2016 and 2020. Indeed by selecting elected members we have an objective criteria that defines the political affiliation to the speaker of a quote. 

Also, all congressmen that were not reelected in the midterm 2018 elections or that quitted their position are removed from the dataset. Indeed we want to make sure that each elected official has the same timeframe. 

On top of that, we decided to remove the president and vice president from the dataset. Indeed, news outlets would tend to give more speech time to the president of a nation regardless of his political affiliation. And this would bias the result as the party of the president would be over-represented.

Note that we did not take the political parties from the data provided in speaker_attributes as we saw it was incomplete. Also, we planned to only keep the parties Democrat and Republican as the Independent party only contains one politician from 2016 to 2020.

### Methods
For research question 1): Handling text (for now, this was done using natural language toolkit available for python, but more methods will come during Lectures 10 and 11)
For research question 2): Regression analysis (study the “sentiment score” ie. positivity, negativity or neutrality of one quote according in the light of the speaker attributes
For research question 3): Visualisation of data with adequate plots (histograms, box plots, barplots etc.)


### Proposed timeline
W9 Investigate political subjects, use QIds to define quotes that belong to one subject, clean and remodel data
W10 Initial analysis following research questions
W11 Final analysis following research questions
W12 Make nice plots and think of ways to present results
W13 Work on the deliverable aspect

### Organization within the team
Each one of us will investigate one policy (gun laws, climate change…) by generating the maximum possible dataset that contains some vocabulary associated with the topic of the policy. Then once we have picked one or multiple policies, we shall proceed with the analysis, where each of us will take a research question. The last person of the group will take care of defining the quotes that belong to the chosen subjects, clean and remodel the data and focus on the final deliverable.

### File descriptions on git
<ul>
  <li> <em>dataset_extraction</em>: folder that contains the csv files of our dataset (quotes from US congressmen from 2016 to 2020. </li>
  <ul>
    <li> <em>data_filtering</em>: from the loaded data of Quotebank’s drive, this notebook filters quotes of congress speakers that were in the 115th and 116th US congress (ie. that were in both meeting legislatures throughout the whole terms). </li>
    <li> <em>.csv</em> files: used to filter quotes as explained above </li>
  </ul>
  
  <li> <em>analysis</em>: folder that contains our initial analysis regarding our project </li>
  <ul>
    <li> <em>initial_analysis_climate</em>: notebook that contains the initial analysis regarding the issue of climate according to the three research questions defined above, done to understand what was in the data and gave us clues about how to transform the data </li>
    <li> <em>observational_studies</em>: notebook that contains initial observational study analysis on the dataset, focusing on finding covariates that may have some influence on our results. The quotes are not taken into account as we only try to analyse the integrity of the dataset we generated. </li>
    <li> <em>visualization_analysis</em>: folder that contains primary visual description of the dataset for each year to discover its structure and quantify values and influences of attributes of interest (e.g. political party, gender, age) </li>
  </ul>
</ul>

### Questions
Should we take into account the subjectivity of newspapers? Newspapers tend to have a political affiliation but can we simply assume that overall, quotes said from members of one party to be representative of the whole party?

Also, do you have any clues on how we can quantify the accuracy of the natural language toolkit, if needed?
