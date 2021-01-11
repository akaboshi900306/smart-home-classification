# smart-home-classification
# Problem Statement: 

Certifing SKUs as Smart Home is time consuming/lengthy process。
Can we apply some traditional Machine Learning techniques to help automate/assist with this process？


# Background: 

The process that has been setup to tag individual SKUs as "Smart Home" is as followed: 
1) Vendor goes into IDM and marks there product as "Smart Home" 
2) The Merchant gets notified and certifies the product as "Smart Home Certified" if it fits their list of criteria
The Vendor may or may not be incentivized to incorrectly tag there SKU as Smart Home The merchant might accidently tag a SKU as Smart Home 
when it fact it isn't 


Alternative Solution: Have a set list of criteria that an observed SKU needs to meet in order to be marked as "Smart Home Certified" 
If the product doesn't meet that list of criteria, but gets marked as "Smart Home" by the Vendor then provide a prediction from our model 
to help better assist the merchant in the decision making process 


# Methodology：

# 1) What are we predicting? 

We are trying to predict how likely a SKU tagged as "Smart Home" by the Vendor will convert to "Smart Home Certified" 


# 2) What data are we modeling after?

We are using Product Overview data which consists of bullet points, marketing material, and some brief product 
attribute data 

# 3) Data Preprocessing 

Here we apply some natural language processing techniques such as Tokenization, Lemmatization, and Stemming Tokenization: is, a function that will split your text into single words and removes punctuation 


# Lemmatization: 
words in third-person are changed to first person, and verbs in past and future tenses are changed into present (for example, goes, went, and gone all become go) 


# Stemming: 
removes the inflection, reducing the word to its root (for example, shoes becomes shoe)


# 4) TFIDF Vectorization 
In a nutshell this an algorithm to extract features in text and transforms text into a meaningful representation of numbers 
# 5) Model: 

# Random Forest 
Pros: Non Linear Model Do not have to scale variables Robustness to outliers Does not assume data is normally distributed 
Averages Predictions together (wisdom of the crowd) Perform Automatic Feature Selection Suggests a good indicator of feature importance Quick to train 
Can handle large amounts of data 
Cons: Black Box Not easily interpretable Models can take up larges amounts of space (GB, MB) based on the amount of trees in the forest """
