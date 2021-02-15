# ![General Assembly](https://github.com/dylanlee91/DSI-Ames-Housing/blob/main/ga_logo.png?raw=true) Project 3: Using natural language processing to classify posts on r/running and r/Swimming

## Introduction
This is a proof of concept exercise that uses natural language processing to identify posts that are made on two reddit subreddits, r/running and r/Swimming.

## Problem Statement
Being able to identify the fitness interests of internet users can enable the construction of recommendation engines that send the users targeted ads or links.
How might we identify what kind of physical activities are being discussed?
We are looking to construct a model can suitably identify contextual words used alongside a discussion on either activity, without looking for word stems of either activity, such as run, ran, running, runner, swim, swam, swimming, swimmer
If a suitable model and methodology is found, this can be extended to other activities such as biking or weightlifting to develop a more comprehensive recommendation system.

## Executive Summary
1000 posts from the two subreddits were webscraped
The posts were filtered for duplicates and media posts
A random sample of 750 text posts were taken from each subreddit
The self text content of there posts were filtered for stop words as well as words clearly identifying the activity, before being stemmed
The posts were split into training and testing sets
Various models were tested to see which were the most successful at classifying test posts into their respective subreddits
The misclassified posts were investigated

## Selected Results

Here are some of the visualized outputs. The rest are in the Jupyter notebook

![Swimcloud](https://github.com/dylanlee91/DSI-Reddit-Scraping/blob/main/images/Swimcloud.png?raw=true)
![Runcloud](https://github.com/dylanlee91/DSI-Reddit-Scraping/blob/main/images/runcloud.png?raw=true)

![Runstems](https://github.com/dylanlee91/DSI-Reddit-Scraping/blob/main/images/Runstems.png?raw=true)
![Swimstems](https://github.com/dylanlee91/DSI-Reddit-Scraping/blob/main/images/Swimstems.png?raw=true)



## Conclusion and Comments

### Limitations
The posts available to the model are reflective of the demographics of their respective userbases
Swimming is more niche and there are many more posts about technique and competing
It also appears to have many more young athletes as a percentage of the user base
Running has more hobby runners and the discussion topics are broader and less focused
The model is currently only being tested on the source communities
Testing on different communities and different demographics might cause the model accuracy to drop significantly
Demographic concerns include both reddit as a whole and the respective subreddit user bases
Active posters on reddit tend to be much more likely to be below 30
Given that Logistic Regression can only make predictions between two classes, accuracy and the necessity of using a model capable of multiple category classification will decrease in broader applications


### Further Considerations
The results from this project show promise for classifying the word content of user posts into a useful prediction system
The application will be even more applicable with additional training, additional subjects as well as some method for interaction terms (that I have not learned yet)
For example: kick + lap probably indicates swimming technique, kick + gait probably indicates a discussion about running technique, kick + pads probably indicates a kickboxing discussion,
Further controls for communities or training on local data from the target communities would improve accuracy.