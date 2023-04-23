# Railway-Example
## Problem Diagram
### Description
$R:Fence\ Control$: The requirement of this example.  
$Train\\ !\\ \\{Train\\_appraoch,\\ Train\\_in,\\ Train\\_leave\\}$: The domain $Train$ can trigger 3 shared phenomena, i.e. $Train\\_appraoch$, $Train\\_in$ and $Train\\_leave$  
$Train\\_appraoch\rightarrow Train\\_approaching$: If the domain $Sensor$ observes the $Train\\_appraoch$, it will trigger the shared phenomenon $Train\\_approaching$.
$Control\\ Machine$: The machine to be built.
![](https://github.com/Wei-GXNU/Railway-Example/raw/main/Problem%20Diagram.png)
## Fault Tree
![](https://github.com/Wei-GXNU/Railway-Example/raw/main/Fault%20Tree.png)
## Fault Information Mapping Table
ID: Unique identifier for each element in FIMT.  
Name: The identifier of atomic event in FT.  
Type: A mark to identify whether an event in FT can be associated by a shared phenomenon in PD. The value should be set to "Detectable" or "External".  
Domain: The domain in PD that triggers the shared phenomenon.  
Shared Phenomenon: The name of triggerd shared phenomenon.  
|ID|Name|Type|Domain|Shared Phenomenon|
|:-:|:-:|:-:|:-:|:-:|
|E1|X1|Detectable|Car|$Car\\_in$|
|E2|X2|External|$-$|$-$|
|E3|X3|Detectable|Train|$Train\\_in$|
|E4|X4|External|$-$|$-$|
|E5|X5|Detectable|Fence|$Fencec\\_closed$|
|E6|X6|External|$-$|$-$|

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

## A Valid Fault Scenario

$$
\begin{aligned}
Car\\_in\rightarrow \underline{\mathbf{E1}}\rightarrow X1\searrow \\
Train\\_approach\rightarrow Train\\_approaching\rightarrow Fence\\_off\rightarrow Fence\\_closed\rightarrow \underline{\mathbf{E5}}\rightarrow X5\rightarrow \\
Train\\_in\rightarrow \underline{\mathbf{E3}}\rightarrow X3\nearrow 
\end{aligned}
Cutset\rightarrow Topevent
$$  
