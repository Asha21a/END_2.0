<h3> 1) What is a neural network neuron? </h3> 
            1. A neural network neuron is an unit that holds a weight and an activation function. <br/>
            2. Each neuron has both input and output connection. <br/>
            3. With given weight(w) and activation function(tanh), output of a neuron is calculated as <br/> 
                  z=tanh(∑<sup>n</sup><sub>i=1</sub> x<sub>i</sub>w<sub>i</sub>+b)  , where n- number of connections coming in, x- input, b- bias <br/>
            5. The activation fnction can be tanh, sigmoid, ReLU, etc.


<h3> 2) What is the use of the learning rate? </h3> 
           1. Learning rate is a configurable parameter used to train the neural network.
           2. It cannot be too small or too big. It should be an optimal value.
           3. Learning rate is used as follows
w<sup>new</sup><sub>i</sub> = w<sup>old</sup><sub>i</sub> - Learning_rate * [partial_derivative(Error)/ partial_derivative(w<sup>old</sup><sub>i</sub>)]


<h3> 3) How are weights initialized? </h3>



<h3> 4) What is "loss" in a neural network? </h3>



<h3> 5)  What is the "chain rule" in gradient flow? </h3>



