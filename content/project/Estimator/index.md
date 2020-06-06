---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Estimator"
summary: "Estimator is a Machine Learning enabled platform to estimate critical chain length of a polymer corresponding to its saturated solubility parameter."
authors: ["admin"]
tags: ["Machine Learning", "Polymers"]
categories: []
date: 2020-05-25T15:14:21+05:30

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---
Estimator is a Machine Learning enabled platform to predict critical chain length of a polymer corresponding to its saturated solubility parameter.

Checkout the product -
[Estimator](https://polypredictor.herokuapp.com/)

Cover Image Credits - 
[Science-In-Chains](https://science-in-chains.natfak2.uni-halle.de/microscopic-insight/)

# Introduction
Now-a-days machine learning is extensively being used by researchers to accelerate the development process of novel materials. Development of novel polymers can also be accelerated by using machine learning algorithms in many ways. i.e.

1. Predicting properties of a novel polymer before synthesizing it in the laboratory.
2. Tuning the design of a polymer to have desired set of properties.
3. Extracting valuable information from failed experiments by traning ML models.
4. For accelerating material simulation & materials design models (CGM, PSO etc.)

So, whenever we have sufficient amount of data and we need to extract some valuable information from that or need to make some prediction, we can use appropriate machine learning algorithm.

## Problem Statement
The problem on which this project is based on is predicting critical chain length of a desired polymer corresponding to its saturated solubility parameter.

#### Critical Chain Length & Saturated Solubility Parameter
Solubility parameter of a polymer depends on its chain length and after a certain chain length it becomes saturated (no more significant change) more details can be found in literature

Now the issue is the calculation of this value which involves molecular simulations. This process is very slow, computesionaly expensive and inefficient. Our apporach is to solve this problem using machine learning so that we can directly predict the chain length at which the solubility parameter of a polymer will become saturated.

## Machine Learning based solution
So, we are trying to train a machine learning model on a dataset which is having the data of polymers and their critical chain length. The very first issue is making such dataset because we need all the data in mathematical form. We used group conribution theory and developed a python program which is used extract features from a repeting unit structure and make a fingerprint of that polymer using feature vectors and ultimately represents the polymer in numerical form. So, the processed dataset have numerical representation of a polymer and its critical chain length.

Next we are developing a machine learning model from scratch to learn the dependency of critical chain length on various features. Firstly we used linear hypothesis for this purpose because we need continuous outputs. Now we are working on support vector regression model to get better efficiency. We are also working on self evolving machine learning algorithms.

#### Challenges
1. Appropriate numerical representation of a polymer (Using some optimization algorithm)
2. Collecting sufficient amount of data (Using data augmentation techniques)
3. Optimizing number of features to train the model. (Literature Survey Going On)
4. Mapping function to map features vectors to desired property. (Literature Survey Going On)
