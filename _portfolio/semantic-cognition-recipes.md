---
title: "Semantic Cognition on Recipes and Cuisines Around the World"
date: 2019-05-13
excerpt: "The parallel distributed processing approach to semantic cognition: a comparative extension to a complex domain.<br/><img src='/images/SemanticNet.png' style='width:300px;height:254px;'>"
collection: portfolio
---

## Summary

Semantic cognition describes the cognitive mechanism by which humans develop and store object-property associations in long-term memory, and our subsequent ability to generalize from these characteristics to ”identify” objects in terms of trait similarity with previously-observed objects. We engineer a larger and more complex data-set for training within a baseline parallel distributed processing (PDP) architecture, exploring the nature of semantic cognition in the domain of food.

Report can be found [here](https://github.com/zivschwartz/SemanticCognitionRecipes/blob/master/schwartz-taylor-deshpande-laad-ccm-final.pdf), and relevant code can be found [in this GitHub repo](https://github.com/zivschwartz/SemanticCognitionRecipes).

**Data and Methods** 

The computational design of this network includes an encoding process; input items are expressed in a pseudo-binary capacity and passed into a linear ”Representation” layer using rectified linear unit activation (ReLU), bundled with relational features (e.g., ”Canary CAN”) into a single string of 0s and 1s, passed through a single linear hidden layer with ReLU activation, and finally into a linear output layer with Sigmoid activation of corresponding attributes.

<p align="center">
  <img width="485.5" height="381" src="/images/SemanticNet.png">
</p>

Initial data is obtained from [What's Cooking](https://www.kaggle.com/c/whats-cooking) and consists of 39, 774 common recipes belonging to 20 distinct cuisines. We then proceeded to add the following binary (yes or no) labels:
- Vegeterain, Vegan, Spicy, Dessert, Drink

The data is preprocessed to group together similar ingredients found in the cousine (red and green peppers --> bell peppers) and to retain distinctness in other cases (black pepper remains the same).  

Models Fit (parameters hypertuned):
1. Baseline: feed-forward neural network
2. Extension: feed-forward neural network with an extra hidden layer

This consists of four linear layers: 
- one input layer
- two hidden layers (called representation layer and hidden layer respectively) 
- output layer. 

The first 26 entries in each row are input patterns that the network uses to learn; representations of these items are learned using their mappings to the ingredients, which are the output patterns or ground truth labels. ReLU activation is used for the representation and hidden layers. The output layer, however, makes use of Sigmoid activation. To clarify, the output pattern can be thought of as a predicted set of ingredient labels.

Each permutation of data set type 1 model architecture was tested. The representations for each item (cuisine) were extracted after having trained each model for 500, 2500, and 5000 epochs respectively. The patterns are compared in order to find the two that are closest to each other by virtue of a Euclidean distance measure. Subsequently, it iterates over the patterns, replacing each closest pair with an average over that pair, until an underlying pattern remains.

<p align="center">
  <img width="485.5" height="381" src="/images/SemanticDendograms.png">
</p>

To summarize, Human beings learn to differentiate between objects by way of example, storing certain generalized representations of their attributes that aid in categorization, when required. For example, a child that has only seen 2 distinct bird species in her lifetime, both flighted, would make the reasonable assumption that the object category bird must have the attribute flight. However, an adult, presumably exposed to a larger number of distinct bird species, may not make the same generalization. Given a set of ingredients and asked to attribute this with a cuisine label, an individual’s response may (1) be biased toward cuisines they have been exposed to, and (2) not be a single cuisine, as individual ingredients are (for this purpose) atomic and far removed from any generalization of a cuisine.


 
