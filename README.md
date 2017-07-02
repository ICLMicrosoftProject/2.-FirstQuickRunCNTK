# FirstQuickRunCNTK
Introduction to some basic commend lines and quickly dive into cntk. However these exact codes and details can be found and is orignially from the [official site](https://cntk.ai/pythondocs/gettingstarted.html)

## I. What is CNTK?:
Microsoft Cognitive Toolkit, also known as CNTK, is a deep learning framework developed by Microsoft Research. CNTK describes neural networks with composing simple building blocks, which later transformed into complex computational networks to achieve complex deep models with satisfactory performances. The Microsoft’s internal team is using the exact same tool as the one that open sourced to the public. So far, CNTK supports only for Windows and Linux users. we can call the library of CNTK from Python, C++ and .NET. 

## II. Something to try out on your terminal:
Open up your terminal and type in
```
python
```
import cntk with the following and get started.
```
import cntk
```
#### step 1. test version:
```
cntk.__version__
```
#### step 2. Minus() and evaluation() function
```
cntk.minus([1, 2, 3], [4, 5, 6]).eval()
```
key observation: minus().eval()

#### step 3. Set up variables and load data onto the variables with numpy
```
import numpy as np
x = cntk.input_variable(2)
y = cntk.input_variable(2)
x0 = np.asarray([[2., 1.]], dtype=np.float32)
y0 = np.asarray([[4., 6.]], dtype=np.float32)
cntk.squared_error(x, y).eval({x:x0, y:y0})
```
key observation: vairable(), squared_error()

#### step 4. asarray is available
```
import cntk as C
c = C.constant(3, shape=(2,3))
c.asarray()
np.ones_like(c.asarray())
```
Key observation: asarray()

Notes: require more in depth discussion

## III. Something to run with shell:
A fully connected neural net example
 
#### step 1. 
create a file, copy and paste (or download )the [following codes](simplenet.py), save it as simplenet.py .


#### step 2. 
go to terminal and type 
```
python simplenet.py
```


## Reference
[1] https://cntk.ai/pythondocs/gettingstarted.html
## Claim
The instruction and codes are originally from the [official website](https://cntk.ai/pythondocs/).
This is just a quick guide of how student would approach the tool.
