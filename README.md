# Railway-Example
## Problem Diagram
![](https://github.com/Wei-GXNU/Railway-Example/raw/main/Problem%20Diagram.png)
## Fault Tree
![](https://github.com/Wei-GXNU/Railway-Example/raw/main/Fault%20Tree.png)
## Fault Information Mapping Table

|ID|Name|Type|Domain|Shared Phenomena|
|:-:|:-:|:-:|:-:|:-:|
|E1|X1|Detectable|Car|$Car\\_in$|
|E2|X2|External|Car|$-$|
|E3|X3|Detectable|Train|$Train\\_in$|
|E4|X4|External|Fence|$-$|
|E5|X5|Detectable|Fence|$Fencec\\_closed$|
|E6|X6|External|Sensor|$-$|

## Causal Chain set / Causal Chains

- $Train\\_approach\rightarrow Train\\_approaching\rightarrow Fence\\_off\rightarrow Fence\\_closed$  
- $Train\\_leave\rightarrow Train\\_left\rightarrow Fence\\_on\rightarrow Fence\\_opened$  
- $Train\\_in$  
- $Car\\_approach$  
- $Car\\_in$  
- $Car\\_leave$  


## Minimal cut sets
$\\{X1,X2,X3\\}$  
$\\{X1,X4,X3\\}$  
$\\{X1,X5,X3\\}$  
$\\{X1,X6,X3\\}$  

## A Valid Fault Scenario Chain

$$
\begin{aligned}
Car\\_in\rightarrow \underline{\mathbf{E1}}\rightarrow X1\searrow \\
Train\\_approach\rightarrow Train\\_approaching\rightarrow Fence\\_off\rightarrow Fence\\_closed\rightarrow \underline{\mathbf{E5}}\rightarrow X5\rightarrow \\
Train\\_in\rightarrow \underline{\mathbf{E3}}\rightarrow X3\nearrow 
\end{aligned}
Cutset\rightarrow Topevent
$$  
