---
title: Tidy Data with Pandas
date: 2022-01-30
layout: post
category: General
---

#### What did the author try to accomplish?

The author, Hadley Wickham, wanted to improve upon the idea of data cleaning - naming it “data tidying”. He argues that having a standard way of keeping data tidy helps make the necessary, but cumbersome task of data cleaning more effective and efficient. He outlines and gives examples of why he thinks tidy datasets are easier to manipulate, visualize, and model. For this paper, he tries to accomplish this with a thorough explanation of what tidy data is and the justifications for why it’d be necessary and useful.

#### What were the key elements of the approach? 

The first part of the approach would be to define what tidy data is and what it looks like. According to Wickham, tidy data has an ideal “specific structure: each variable is a column, each observation is a row, and each type of observational unit is a table.” As a novice in data science, I would interpret that to be each feature, like a column in a table, each observation/ each unit of data that is of itself has its own row, for example, in a housing data set, each house as a row. And lastly, each type of observation has its table. 

|             | Sex  | Weight | Color         |
|-------------|------|--------|---------------|
| Mugi_cat1   | Male | 13 lbs | Tabby         |
| Smudge_cat2 | Male | 15 lbs | Black & White |

<br> 
#### What can you use yourself? 

The examples given in the paper are mostly focused on the programming language R. I haven’t worked with R yet as a beginner, but do have some experience with pandas and python. I will explain in the context of pandas. The first would be to manipulate untidy data. With pandas, you can manipulate a data frame by melting and stacking as the author explained (using R). 

Some pandas methods to manipulate data include:

- pd.melt - This method essentially takes a wide dataset and reduces it to a long dataset. Moving columns into rows. 

- pd.stack - This method addresses multi-level columns that moves a level to an index position, making a multi-index.

- pd.unstack - This method takes an inner level index and moves it to be on another level on the columns. 

Another way you could tidy the multi-indexed table would be by using pd.reset_index, which would take the different indices and create them as new columns.

#### What other references do you want to follow?

For this paper, there are not many other references I’d like to follow up on. Mainly because the paper was written for the R programming language. 

 

