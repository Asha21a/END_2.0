<h3> 1) What is a neural network neuron? </h3> 
            1. A neural network neuron is an unit that holds a weight and an activation function. <br/>
            2. Each neuron has both input and output connection. <br/>
            3. With given weight(w) and activation function(tanh), output of a neuron is calculated as <br/> 
                  z=tanh(∑<sup>n</sup><sub>i=1</sub> x<sub>i</sub>w<sub>i</sub>+b)  , where n- number of connections coming in, x- input, b- bias <br/>
            5. The activation fnction can be tanh, sigmoid, ReLU, etc.


<h3> 2) What is the use of the learning rate? </h3> 
           1. Learning rate is a configurable parameter used to train the neural network. <br/>
           2. It cannot be too small or too big. It should be an optimal value. <br/>
           3. Learning rate is used as follows <br/>
w<sub>i</sub><sup>new</sup> = w<sub>i</sub><sup>old</sup> - Learning_rate * [partial_derivative(Error)/ partial_derivative(w<sub>i</sub><sup>old</sup>)]


<h3> 3) How are weights initialized? </h3>
            1. Weights are initialized as small random values from standard normal distribution. <br/>


<h3> 4) What is "loss" in a neural network? </h3>
            1. Loss in a neural network is a number indicating how bad the model prediction is. <br/>
            2. If loss = 0, it means the model prediction is good. <br/>
            3. If loss >0, it means the model prediction is bad. <br/>


<h3> 5)  What is the "chain rule" in gradient flow? </h3>
            If a variable 'z' depends on variable 'y', which in turn depends on variable 'x', then it means variable 'z' depends on variable 'x' via variable 'y' <br/>
            In derivative terms, it is written as follows. <br/>
            derivative(z)/derivative(x) = [derivative(z)/derivative(y)] * [derivative(y)/derivative(x)]


