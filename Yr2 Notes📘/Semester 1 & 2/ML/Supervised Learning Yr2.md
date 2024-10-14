# Supervised Learning Yr2
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::2]. Contains details on when this was created, what module the note belongs to.
> > *Date :*  01-10-2024
> > *Module :* [[Machine Learning]]
> > *Teacher*: 
> > *Resources :*

---
> [!abstract]+ Contents
> List of headings within this topic
> > [[#Speed run]]
> [[#Types of Learning]]
> [[#Supervised Learning]]
> [[#Unsupervised Learning]]
> [[#Reinforcement Learning]]
> [[#Creating a Supervised Learning Model]]

--- 
> [!danger]+ *Speed run*
> Break down of topic 
> > $a)$ -  Supervised - Learns though ==Example==
> $b)$ - Unsupervised - Learning the ==structure== from ==data==
> $c)$ - Reinforcement - Learning through ==Trial== and ==Error==

---

#TODO 

### Types of Learning

#### Supervised Learning
Learns through examples 
E.g Rainfall Forecast, Classifiying Fraud Transactions, OBject Detection

#### Unsupervised Learning 
Structure of data
E.g Anomaly detection, Natural Language Processing, Customer Segmentation

#### Reinforcement Learning
Trial and Error
E.g Personalised Learning, Gaming AI,Traffic Control


## Creating a Supervised Learning Model

In order to create a model we need a few things

| Type of model                                                             | Cost Function                                                                         | Optimiser                                                    |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| Determines how we make predictions. <br>• Parametric <br>• Non-parametric | The cost-function determines how good our model is based on the predictions it makes. | The optimizer determines how we modify and improve our model |
![[Basics of training.png]]

## E.g Linear Regression

Hypothesis Function $h_\theta(x) = \sum\theta^Tx$
Cost function $𝐽(θ) = \frac{1}{2𝑚}\sum_{𝑖=1}^𝑚 (ℎ_θ(𝑥^𝑖 )−𝑦^𝑖)^2$ 
