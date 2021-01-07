Scope slide3 and note2

**key words**: Linear classification, Linear score function, three types Loss function.

1. Since KNN algorithm has a number of disadvantages, we are now going to develop a new and powerful approach to image classification: Linear classification. Two main components of it are score function and loss function.
2. Score function has the formula  below:


$$
f(W,x_i,b)=Wx_i+b
$$
$x_i$ is a $n\times1$ row which we get from stretching a matrix of a pixel. Essentially, every row of W is a weight vector for pixel with respect of every class. So we are trying to select the fittest class based on the sum of the multiplication of the special weight row and the pixel column. On the other hand, we can also see a row of W as a template and the classification process as finding the fittest template. For bias, we can use a trick such as adding a column to W and extend $n\times1$ $x_i$to $(n+1)\times 1$  $ x_i$ so that we can simply use one matrix.

3. Loss function is a method to evaluate our prediction. For SVM(support vector machine) we have the formula below.
   $$
   L_i=\sum_{j\neq y_i}max\{0,s_j-s_{y_i}+\delta\}
   $$
   where s is the abbreviate of score and $y_i$ is the ground true class. $\delta$ is the margin and unless the score of true class is greater than all other class's score or there will be loss. In other words, $\delta$ is a judging factor. Moreover, we can exchange $s_i$ with score function. 

   Most time we will add a regularization parameter to avoid ambiguity. We usually use $L_2$ norm penalty as below.
   $$
   R(W)=\sum_{k}\sum_{l}W_{k,l}^2
   $$
    It has many excellent properties we will see later.

   Last, we get the final formula of SVM loss function.
   $$
   L=\frac{1}{N}\sum_{i}L_i+\lambda R(W)
   $$
   where N is the size of training data.

   

 

