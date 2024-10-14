# Advanced ML
---
> [!info]+ File Details
> Includes information about this (genus:: Note) from [Year::1]. Contains details on when this was created, what module the note belongs to. 
> >*Date :* 22-06-2024
> > *Module :* (ModCode :: CM12001) 
> > *Teacher*: 
> > *Resources :* #Chatted

---
> [!abstract]+ Contents
> List of headings within this topic
> [[#Speed run]]
> [[#Neural Networks]]
> [[#Backpropagation]]
> [[#Overfitting]]
> [[#Regularization]]
---
### Speed Run

1. Break down of topic
	$a)$ **Neural Networks** - Neural networks are a set of algorithms, modeled loosely after the human brain, that are designed to recognize patterns
	$b)$ **Backpropagation** - Backpropagation is the algorithm for supervised learning of artificial neural networks using **gradient descent**
	$c)$ **Overfitting** - Overfitting is a **modeling error** in machine learning where a function is **too closely fit** to a limited set of data points, resulting in a model that performs well on training data but poorly on unseen data
	$d)$ **Regularization** - Regularization involves adding a penalty term to the loss function to prevent overfitting by discouraging complex models
---

### Detailed Explanation

#### Neural Networks
Neural networks are a set of algorithms, modeled loosely after the human brain, that are designed to recognize patterns. They interpret sensory data through a kind of machine perception, labeling, or clustering of raw input. Neural networks consist of layers of interconnected nodes where each connection has a weight that is adjusted during training. They are widely used in various applications such as image and speech recognition, natural language processing, and autonomous systems.

#### Backpropagation
Backpropagation is the algorithm for supervised learning of artificial neural networks using gradient descent. It computes the gradient of the loss function with respect to each weight by the chain rule, iteratively adjusting weights to minimize error. The process involves a forward pass, where inputs are propagated through the network to compute outputs, followed by a backward pass, where gradients are calculated and used to update weights. This method is essential for training deep neural networks efficiently.

#### Overfitting
Overfitting is a modeling error in machine learning where a function is too closely fit to a limited set of data points, resulting in a model that performs well on training data but poorly on unseen data. Overfitting can occur when a model is excessively complex, capturing noise rather than the underlying data pattern. Techniques such as cross-validation, pruning, and regularization are used to detect and prevent overfitting, ensuring the model generalizes well to new data.

#### Regularization
Regularization involves adding a penalty term to the loss function to prevent overfitting by discouraging complex models. Common techniques include L1 (Lasso) and L2 (Ridge) regularization, which add penalties proportional to the absolute or squared values of the weights, respectively. These techniques help in maintaining a balance between fitting the training data and keeping the model parameters small, thereby improving the generalization of the model.

---