
### Multiplexers(MUX)  
---
* It is combinational cirrcuit that selects binary information from one of man input lines and directs it to output line<br>
* It is Simply  a data Selector <br>

### Advantages :
  1.Reduces circuit Complexity and cost <br>
  2.Reduces No. of Wires <br>
  3.Implementation of various Circuit using Mux.<br> 

#### 2 X 1 MUX :

| E  | S | Y |
|----|---|----|
|0|X| 0| 
1|0| I<sub>0</sub>| 
|1|1| I<sub>1</sub>| 

<br> 

 #### Visulization : 

 <br> 

![circuit diagram](./multiplexer.png) 

<br> 
#### output : 
Y = E . S*. I<sub>0</sub> + E. S*. I<sub>1</sub> <br>

Y = E (S*. I<sub>0</sub> +S*. I<sub>1</sub>) <br> 
#### Circuit Diagram  : 
<br> 

![circuit diagram](./circuit%20diagram%202%20X%201%20.png)  
<br> 


#### 4 X 1 MUX : 

| E  | S | Y | 
|----|---|---| 
|0|0|I<sub>0</sub>|
|0|1|I<sub>1</sub>|
|1|0|I<sub>2</sub>|
|1|1|I<sub>3</sub>| 
<br> 



#### Visulization :


![circuit diagram](./4X1multiplexer.jpg ) 

#### output :
 Y = s<sub>1</sub>* s<sub>0</sub>* I<sub>0</sub> + 
s<sub>1</sub>* s<sub>0</sub> I<sub>1</sub> + s<sub>1</sub> s<sub>0</sub>* I<sub>1</sub> + s<sub>1</sub> s<sub>0</sub> I<sub>3</sub> <br> 
<br> 

#### Circuit Diagram  : 
<br> 

![Circuit diagram](./4_1_multiplexer_circuit_diagram.jpg) 
<br> 

### 8 X 1 MUX  : 
|S<sub>2</sub> |S<sub>1</sub> |S<sub>0</sub> | Y | 
|---------|---------|---------|----| 
|0|0|0|I<sub>0</sub>| 
|0|0|1|I<sub>1</sub>|
|0|1|0|I<sub>2</sub>|
|0|1|1|I<sub>3</sub>|
|1|0|0|I<sub>4</sub>|
|1|0|1|I<sub>5</sub>|
|1|1|0|I<sub>6</sub>|
|1|1|1|I<sub>7</sub>|
<br>  
#### Visulization : 
![circuit diagram](./multiplexer%208%20X%201.png)  
<br> 

 #### output : 
 Y = s<sub>2</sub>* s<sub>1</sub>* s<sub>0</sub>* I<sub>0</sub>+ s<sub>2</sub>* s<sub>1</sub>* s<sub>0</sub>* I<sub>1</sub> + s<sub>2</sub>* s<sub>1</sub>* s<sub>0</sub>* I<sub>2</sub> + s<sub>2</sub>* s<sub>1</sub>* s<sub>0</sub>* I<sub>3 </sub> + s<sub>2</sub>* s<sub>1</sub>* s<sub>0</sub>* I<sub>4</sub> + s<sub>2</sub>* s<sub>1</sub>* s<sub>0</sub>* I<sub>5 </sub> + s<sub>2</sub>* s<sub>1</sub>* s<sub>0</sub>* I<sub>6</sub> + s<sub>2</sub>* s<sub>1</sub>* s<sub>0</sub>* I<sub>7</sub> <br> 

<br>

#### Circuit Diagram :  
![circuit diagram](./4_1_multiplexer_circuit_diagram.jpg) 





