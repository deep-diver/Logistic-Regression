# Simple Neural Network without hidden layer

This repository is to demonstrate a simple neural networks without hidden layers. All the functions to build the neural networks are written in numpy.

### The flow
1. **main** function
 - get the image datasets, then flatten and normalize them.
 - build and train the model
 - print out relative informations
2. **model** function
 - initialize parameters by calling **initialize_with_zeros** function
 - optimize the parameters by training on the training dataset. This is done by calling **optimize** function
 - run prediction on training and testing datasets by calling **predict** function
 - return cost, predictions, updated w and b, and etc.
3. **initialize_with_zeros** function
 - simply initialize the parameters, w and b
 - this is done by **numpy.zeros** function
4. **optimize** function
 - iterating for the number of iterations given as a hyper-parameter
 - while iterating it calculates gradient decent and costs by calling **propagate** function. also, update the parameters, w and b with the calculated gradient decent
 - return the final values of parameters and gradient decent
5. **propagate** function
 - performs calculation in the following order
  - **sigmoid** function as the activation function on w, X, and b ![alt text](./images/activatoin.png)
  - calculate the cost function J <br/>![alt text](./images/cost.png)
  - calculate the gradient decent on w and b
    - ![alt text](./images/dw.png)
    - ![alt text](./images/db.png)
  - return them
6. **predict** function
 - simply running **sigmoid** function on w, X, and b. with the result of the **sigoid** function (a), it returns 0 if a <= 0.5, and it returns 1 otherwise.
7. **sigmoid** function
 - simply calculate and return <br/>![alt text](./images/sigmoid.png)

### Dependencies
- **numpy**
 - for handy matrix operations
 - http://www.numpy.org/
- **h5py**
 - Pythonic interface to the HDF5 binary data format.
 - Image dataset is stored in h5 file format.
 - https://www.h5py.org/
