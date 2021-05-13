											
							
											
											
											
											
											
											
											
											
											
											
											
![image](https://user-images.githubusercontent.com/83409496/118163080-2d3f6200-b43f-11eb-9018-42cabd2d8667.png)


<b>Steps: </b><br/>

Learning rate, η= 0.5
t1 = 0.01 <br/>
t2 = 0.99 <br/>
i1 = 0.05 <br/>
i2 = 0.1 <br/>
w1 = 0.15 <br/>
w2 = 0.2 <br/>
w3 = 0.25 <br/>
w4 = 0.3 <br/>

h1 = w1*i1 + w2*i2 = ![image](https://user-images.githubusercontent.com/83409496/118169416-8a8ae180-b446-11eb-8552-85e571fabe37.png) <br/>
h2 = w3*i1 + w4*i2 = ![image](https://user-images.githubusercontent.com/83409496/118169579-bc03ad00-b446-11eb-98f7-16ceb4c0d6a4.png) <br/>
a_h1 = σ(h1) = 1/(1+ exp(-h1)) = ![image](https://user-images.githubusercontent.com/83409496/118169686-da69a880-b446-11eb-85f1-31dae544d597.png) <br/>
a_h2=σ(h2) = 1/(1+exp(-h2)) = ![image](https://user-images.githubusercontent.com/83409496/118169765-f1a89600-b446-11eb-81f7-e1fd0520f7a7.png) <br/>
o1 = w5*a_h1 + w6*a_h2 = ![image](https://user-images.githubusercontent.com/83409496/118169924-21579e00-b447-11eb-9014-492f499df22a.png) <br/>
o2 = w7*a_h1 + w8*a_h2 = ![image](https://user-images.githubusercontent.com/83409496/118169958-2e748d00-b447-11eb-9277-de6f71cb96a6.png) <br/>
a_o1 = σ(o1)=1/(1+exp(-o1)) = ![image](https://user-images.githubusercontent.com/83409496/118170028-40eec680-b447-11eb-9673-4fee7244564a.png) <br/>
a_o2 = σ(o2)=1/(1exp(-o2)) = ![image](https://user-images.githubusercontent.com/83409496/118170058-4d731f00-b447-11eb-9cfe-e0ff31661f46.png) <br/>
E1 = ½ * (t1-a_o1)² = ![image](https://user-images.githubusercontent.com/83409496/118170098-582db400-b447-11eb-8d53-9e9fb9f16668.png) <br/>
E1 = ½ * (t2-a_o2)² = ![image](https://user-images.githubusercontent.com/83409496/118170139-62e84900-b447-11eb-8826-6f6f5f250920.png) <br/>
E_total = E1+ E2 = ![image](https://user-images.githubusercontent.com/83409496/118170188-6ed40b00-b447-11eb-802d-759acb67441e.png) <br/>

∂E1/∂a_o1 =∂ (1/2 *(t1-a_o1)^2)/∂a_o1 = (t1-a_o1)*(-1) = a_o1 - t1 <br/>
∂a_o1/∂o1 = ∂(σ(o1))/∂o1 = σ(o1)*(1-σ(o1)) = a_o1 * (1-a_o1) <br/>
∂o1/∂w5 = a_h1 <br/>

∂E_t/∂w5 = (a_o1 - t1) * a_o1 * (1-a_o1) * a_h1 = ![image](https://user-images.githubusercontent.com/83409496/118170800-29640d80-b448-11eb-9968-d0fe017c12a0.png) <br/>
∂E_t/∂w6 = (a_o1 - t1) * a_o1 * (1-a_o1) * a_h2 = ![image](https://user-images.githubusercontent.com/83409496/118170837-3680fc80-b448-11eb-9974-60fcf6e8fc30.png) <br/>
∂E_t/∂w7 = (a_o2 - t2) * a_o2 * (1-a_o2) * a_h1 = ![image](https://user-images.githubusercontent.com/83409496/118170915-4567af00-b448-11eb-91b1-1d6c26d99569.png) <br/>
∂E_t/∂w8 = (a_o2 - t2) * a_o2 * (1-a_o2) * a_h2 = ![image](https://user-images.githubusercontent.com/83409496/118170949-51ec0780-b448-11eb-9a46-d821e36d4431.png) <br/>

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

∂E_t/∂w1 = (((a_o1 - t1) * (a_o1*(1-a_o1)) * w5) + ((a_o2 - t2) * (a_o2*(1-a_o2)) * w7)) * a_h1 * (1-a_h1) * i1 = ![image](https://user-images.githubusercontent.com/83409496/118170281-8b704300-b447-11eb-8cf5-6130d2fb00b4.png) <br/>

∂E_t/∂w2 = (((a_o1 - t1) * (a_o1*(1-a_o1)) * w5 )+ ((a_o2 - t2) * (a_o2*(1-a_o2)) * w7)) * a_h1 * (1-a_h1) * i2 = ![image](https://user-images.githubusercontent.com/83409496/118170716-0e919900-b448-11eb-8540-238b147a3b33.png) <br/>

∂E_t/∂w3 = (((a_o2 - t2) * (a_o2*(1-a_o2)) * w8) + ((a_o1 - t1) * (a_o1*(1-a_o1)) * w6)) * a_h2 * (1-a_h2) * i1 = ![image](https://user-images.githubusercontent.com/83409496/118171665-19006280-b449-11eb-941d-6fd8aa73f129.png) <br/>

∂E_t/∂w4 = (((a_o2 - t2) * (a_o2*(1-a_o2)) * w8) + ((a_o1 - t1) * (a_o1*(1-a_o1)) * w6)) * a_h2 * (1-a_h2) * i2 = ![image](https://user-images.githubusercontent.com/83409496/118171752-33d2d700-b449-11eb-98dd-ebdfd7ad773b.png) <br/>

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
