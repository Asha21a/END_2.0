											
							
											
											
											
											
											
											
											
											
											
											
											
![image](https://user-images.githubusercontent.com/83409496/118163080-2d3f6200-b43f-11eb-9018-42cabd2d8667.png)


<b>Steps: </b><br/>
h1 = w1*i1 + w2*i2 <br/>
h2 = w3*i1 + w4*i2 <br/>
a_h1 = σ(h1) = 1/(1+ exp(-h1)) <br/>
a_h2=σ(h2) = 1/(1+exp(-h2)) <br/>
o1 = w5*a_h1 + w6*a_h2 <br/>
o2 = w7*a_h1 + w8*a_h2 <br/>
a_o1 = σ(o1)=1/(1+exp(-o1)) <br/>
a_o2 = σ(o2)=1/(1exp(-o2)) <br/>
E1 = ½ * (t1-a_o1)² <br/>
E1 = ½ * (t2-a_o2)² <br/>
E_total = E1+ E2 <br/>

∂E1/∂a_o1 =∂ (1/2 *(t1-a_o1)^2)/∂a_o1 = (t1-a_o1)*(-1) = a_o1 - t1 <br/>
∂a_o1/∂o1 = ∂(σ(o1))/∂o1 = σ(o1)*(1-σ(o1)) = a_o1 * (1-a_o1) <br/>
∂o1/∂w5 = a_h1 <br/>

∂E_t/∂w5 = (a_o1 - t1) * a_o1 * (1-a_o1) * a_h1 <br/>
∂E_t/∂w6 = (a_o1 - t1) * a_o1 * (1-a_o1) * a_h2 <br/>
∂E_t/∂w7 = (a_o2 - t2) * a_o2 * (1-a_o2) * a_h1 <br/>
∂E_t/∂w8 = (a_o2 - t2) * a_o2 * (1-a_o2) * a_h2 <br/>

∂E1/∂a_h2 = (a_o2 - t2) * (a_o2*(1-a_o2)) * w8 + (a_o1 - t1) * (a_o1*(1-a_o1)) * w6 <br/>

∂E_t/∂a_h1 = ∂(E1+E2)/∂a_h1 <br/>
∂E1/∂a_h1 = (∂E1/∂a_o1) * (∂a_01/∂o1) * (∂o1/∂a_h1) = (a_o1 - t1) * (a_o1*(1-a_o1)) * w5 + (a_o2 - t2) * (a_o2*(1-a_o2)) * w7 <br/>


∂E_t/∂w1 = (∂ET/∂a_o1) * (∂a_o1/∂o1) * (∂o1/∂a-h1)* (∂a_h1/∂h1) * (∂h1/∂w1) <br/>
∂E_t/∂w1 =  (∂ET/∂a_h1)* (∂a_h1/∂h1) * (∂h1/∂w1) <br/>
∂E_t/∂w1 =  (∂ET/∂a_h1)* a_h1 * (1-a_h1) * (∂h1/∂w1) <br/>
∂E_t/∂w1 =  (∂ET/∂a_h1)* a_h1 * (1-a_h1) * i1 <br/>
∂E_t/∂w2 =  (∂ET/∂a_h1)* a_h1 * (1-a_h1) * i2 <br/>
∂E_t/∂w3 =  (∂ET/∂a_h2)* a_h2 * (1-a_h2) * i1 <br/>
∂E_t/∂w4 =  (∂ET/∂a_h2)* a_h2 * (1-a_h2) * i2 <br/>

∂E_t/∂w1 = (((a_o1 - t1) * (a_o1*(1-a_o1)) * w5) + ((a_o2 - t2) * (a_o2*(1-a_o2)) * w7)) * a_h1 * (1-a_h1) * i1 <br/>


<b>Learning Rate = 0.1 </b> <br/>

![image](https://user-images.githubusercontent.com/83409496/118160794-632f1700-b43c-11eb-9b17-ac6fd725bc0e.png)


<b>Learning Rate = 0.2 </b> <br/>

![image](https://user-images.githubusercontent.com/83409496/118160833-73df8d00-b43c-11eb-89c5-b4b57d001cd9.png)


<b>Learning Rate = 0.5 </b> <br/>

![image](https://user-images.githubusercontent.com/83409496/118162727-b7d39180-b43e-11eb-8e35-46e1bcd420a7.png)


<b>Learning Rate = 0.8 </b> <br/>

![image](https://user-images.githubusercontent.com/83409496/118162892-ed787a80-b43e-11eb-91ce-8af2830e6633.png)


<b>Learning Rate = 1.0 </b> <br/>

![image](https://user-images.githubusercontent.com/83409496/118162937-f8cba600-b43e-11eb-82b3-c72fb30087c5.png)


<b>Learning Rate = 2.0 </b> <br/>

![image](https://user-images.githubusercontent.com/83409496/118160476-fae03580-b43b-11eb-9b4c-b7e9568529f5.png)
