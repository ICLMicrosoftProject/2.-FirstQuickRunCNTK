# FirstQuickRunCNTK
Introduction to some basic commend lines and quickly dive into cntk

##I. Python CNTK documentation:

##II. Something to try out on your terminal:
Open up your terminal and type in
```
python
```
import cntk with the following and get started.
```
import cntk
```
####step 1. test version:
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

##III. Something to run with shell:
A fully connected neural net example
 
step 1. 
create a file, copy and paste the following codes, save it as simplenet.py . 
step 2. 
go to terminal and type python simplenet.py
step 3.
While it is running, check out the explanation
