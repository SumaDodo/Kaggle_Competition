**Recurrent Neural Networks for particle tracking:**

Idea behind RNN - make use of sequential information.
RNNs are called recurrent because they perform the same task for every element of the sequence with output being dependent on previous computations. Keeping track of previous results is a very important part in most of the applications as most of the time they contribute towards the next step/stage of the prediction.  
RNN have memory which captures information about what has been calculated so far.

**Computation in RNN**  
1. x<sub>t</sub> is the input at time step t.
2. s<sub>t</sub> is the hidden state at time step t. It is calculated based on the previous hidden states and the current input.
3. o<sub>t</sub> is the output.

RNN shares same parameters across all steps thus reducing the number of parameters we need to learn.  

**LSTM networks:**  
LSTMs don't have a fundamentally different architecture from RNNs but they use a different function to compute the hidden state.
The memory in LSTMs are called cells and you ccan think of them as blank boxes that take as input the previous state h<sub>t-1</sub> and current input x<sub>t</sub>. Internally the cells decide on what to keep and what to erase.

**LSTM vs. Kalman Filters**  
1. Unlike kalman filter, LSTMs make no assumption about the type of the motion of the object so they should be able to capture both linear and non linear motion.
2. LSTM are discriminative model unlike Kalman filter. Thus they output only a predicted value rather than distribution.

**Idea of two LSTMs for the current problem**  
One to predict the next position and another to predict the varience in that LSTM.
To train the first LSTM, we feed in the previous measurements and use the ground truth as true labels. For the second LSTM, we train on the previous measurements and current prediction and optimize for the o/p.

**Note:** If the momentum is high then, the particle travels th straight path. If less then helical path.  

A very good approach will be to use/ apply decoupled extended Kalman Filter training algorithm to the LSTM architecture. Please find the paper [here](https://github.com/SumaDodo/Kaggle_Competition/blob/master/Resources/lstm%20with%20dekf.pdf)

**References:**  
1. [RNN](http://www.wildml.com/2015/09/recurrent-neural-networks-tutorial-part-2-implementing-a-language-model-rnn-with-python-numpy-and-theano/)
2. [Unsupervised learning in LSTM Recurrent Neural Network](ftp://ftp.idsia.ch/pub/juergen/icann2001unsup.pdf) 
3. [Target Tracking with Kalman Filter, KNN and LSTM](http://cs229.stanford.edu/proj2016/report/IterKuckZhuang-TargetTrackingwithKalmanFilteringKNNandLSTMs-report.pdf)
