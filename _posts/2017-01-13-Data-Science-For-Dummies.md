---
title: "Data Science for dummies"
comments: false
---

# Introduction

My mother often asked me what I did as Data Scientist, what were my everyday tasks, etc... So I am going to try to explain my work.


# The Data Scientist

## His duty
The job of the Data Scientist is to explore data and information to extract from them some value or any other interesting patterns.
It is often said that the Data Scientist is an expert which combine statistics, IT and business expertise being also good in visualization and graphics creation.

The skills of the Data Scientist are often summarize with this diagram:

![Data Science Diagram]({{site.baseurl}}/assets/Data_Science_VD.png)

In reality, it is difficult to possess all these capacities in just one person and most of the time, we regroupe various Data Scientists with individual skills to create a team.


## But why ?
![But why gif]({{site.baseurl}}/images/giphy.gif)

The need for a Data Scientist change a lot according to the business of the company.

In a e-commerce company, he will be able to analyze the customers actions to determine why they buy or don't buy a particular object. He is also going to discover the links between the purchase of the various customers so that the website is then able to offer some personalized products to each customers.

In a gaz transmission company, the Data Scientist will be able to analyze the results of some sensors which records information about the state of the pipeline, the volume carried, the speed of transmission, etc... in order to anticipate eventual accidents.

In the banking domain, he will be able to anlyze the data from the transaction of the customers to determine more easily frauds or personnal customers information (if a French customer suddenly buy for 10 000€ of pizza in a Shangaï restaurant, it is highly possible that the banking information of this customer have been robbed).

# In practice

## The data
The main issue for the Data Scientist is to obtain the data. Without them, he can't do anything. Hopefully, it is more and more easy to find them nowadays. A lot of companies or public institutions give theirs freely. It is called Open Data because it is then possible to do whatever you want from these data.

It is also possible to obtain them thanks to competitions, often organized by companies, but if is often forbidden to use them for commercial purpose.

A lot of data can also be extracted from the web like for Twitter, Facebook, news website or classical web pages but it is mandatory to verify that the websites allow the extraction of their webpage. This technic is called **Web Scraping**.

But most of the time, the Data Scientist works on private entreprise data which are stored over time.

But where these data come from ? Nowadays, companies keep records of almost everything. For example, on most of the e-commerce website, it is common that every action, clic of a customer on the website is saved. Objects tend also to have more and more sensors which record a lot of information to help future improvement (example: new cars are full of sensors which record position, temparature of the oil, temperature of the engine, etc... to allow then the automobile constructors to determine most common issues).


## Data pre-processing
Once the data in our possession, they must be prepared before being able to use them. Raw data are far from being perfect and the format often vary or some of them are missing.
That is why there is almost always a important work of data cleaning which consist in the modification of the data so they can be harmonized and usable.

In addition of this cleaning process, the Data Scientist is sometimes forced to create new data from the existing ones in order to facilitate their interpretations. These new data can be created by the use of a calculation formula or even by splitting a variable in two for example. We call this the **Feature Engineering**.


## The Machine Learning
The final step of the data analysis process is very often a processus called Machine Learning.
Looking by ourselves what the data can tell us can be a very complex and cumbersome work, this is why the machine learning is used so that the computer find by itself a signification to the data or find itself what tie the data.

The machine learning is separated in two groups:

- Supervised Machine Learning
- Unsupervised Machine Learning

### The Unsupervised Machine Learning
This kind of machine learning is used when we have data but we don't really know what to look for, in which direction we want to go.
The Data Scientist is going to put the data he have through an algorithm (a suite of operation and instruction) hoping that the computer is going to find some interesting features.
The most common example is the **clustering** where the machine is going to split the data in groups.

Example of clustering:

- The image on top show various points
- The image on bottom show the groups of points discovered after the use of the clustering algorithm

![kmeans]({{site.baseurl}}/images/kmeans.png)

After the use of the algorithm, we have 3 groups which could be interesting to handle separately.

### The Supervised Machine Learning
At the opposite of the unsupervised, this type of machine learning is used when we know what we are looking for.

I will try to use a simple example:
Lets imagine that we have 100 parrots. For each of the parrot we have:

1. The age
2. The gender
3. The race
4. The color of the bottom left feather
5. If the parrot have a partner
6. If the parrot is smart

The points 1 to 5 can be obtain easily but the point 6 is more complicated because you need to make some test on the parrots.
So we are going to give to our machine learning algorithm just the data from 1 to 5 telling it: with the variables, I want you to find the link with the point 6. The algorithm is going to do its best to obtain the variable 6 thanks to the others. Once that the computer will have learn the best way to obtain what we asked, it will return a function called **model** that we will be able to reuse (N.B. : the unsupervised machine learning also return a model).

Thanks to this model, when a new parrots will come, we will just need to detect its age, sex, race, color of the bottom left feather and if it has a partner or not. We will then give these information to the model which will tell us then if, from what it learned before, the parrots is smart or not, allowing us to earn some precious time.

### Complications
The principal issue of the supervised machine learning is that you need to have some data with already some results you want. These results can be sometimes difficult to find.
Moreover, it is not always possible to predict what we want, there is a high probability that for our parrots example, the computer won't be able to find if the parrot is smart or not thanks to the other information we have and in this case, we will probably need to find some additional data, delete some useless variables or (re)make some feature engineering.


# Conclusion
The work of the Data Scientist is in general cyclic. Most of the time, he will get some data, process them and try to use them thanks to machine learning for example but if he can't get what he want, he is going to restart with some new data which he will need to reprocess and reuse.

It is a work which can seems repetitive but it is very diverse in reality because the data are never the same and it is always mandatory to adapt ourselves to find the best way to handle them. Moreover it is always very rewarding to discover what the data hide and to succeed in the creation of a good model which predict what we want. It should be noted that in general, the Data Scientist doesn't create the machine learning algorithm which are often use for prediction but he knows how they work and have to keep himself up to date of the innovation to find and adapt the one which will be the more performant for its problem.
