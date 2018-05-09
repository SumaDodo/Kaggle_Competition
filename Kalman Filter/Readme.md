**How Kalman Filter Works?**

- It is a general and powerful tool for combining information in the presence of uncertaininty.

Kalman filter is basically to make an educated guess about any dynamic system. Kalman filter does a very good job filtering out all the
messy reality that comes along. It can take advantage of the corelations between crazy phenomena concerning the data a hand. But it's 
important to note that Kalman filter is really good and ideal for systems that are changing continuously as that would require very less
memory [ Just the previous state]. All that is needed to understand the concept of Kalman Filter is Probability and matrices.

**When can we use Kalman Filters?**   
Kalman filters can help when the following conditions are true:

- We can get measurements of a system at constant rate.
- The measurements have an error rate following Gaussian distribution.
- Can devise a mathematical model of the current problem at hand.
- An estimation is needed

**What all do we need what all does it accept?**
- Mathematical model of the system represented by the matrices A,B and H
- An inital estimate about the complete state of the system. Given in the form of vector x
- estimate about the error of the system given as vector P
- General process and measurement error of the system represented by the matrices: Q and R

**Understanding the Mathematics:**  
Kalman Filter calculates and predicts multiple values  
1. State Prediction: Predict the forthcoming state  
2. Covariance Prediction: Prediction of the error  
3. Innovation: Compare reality vs. prediction  
4. Innovation Covarience: Compare real error against prediction  
5. Kolman Gain: Moderate the prediction  
6. State Update: Update where we are  
7. Covariance Update: New estimate of error  


