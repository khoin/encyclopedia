---
layout: blank
---

{% include mathjax.html %}
<style>
    * { font-family: "MJX_Main";}
    blockquote { 
        border-left: 4px solid #444; margin-left: .5em; padding-left: 1em;
    }
</style>

## Koi Nil // koi@uw.edu // **Math 309** // Problem Set 1 // Jan 8th 2018

### 2.1. Review Questions.

1. Is $$\pmatrix{1\\2\\3}$$ in the span of ...
> Yes. 
> If we represent the given collection as columns of vectors of a matrix 
> $$
    \begin{bmatrix}
    1 &  0 & 2 \\
    2 & -3 & 3 \\
    0 &  1 & 1 \\
    \end{bmatrix}
$$ and then perform row operations on it, we get: $$
    \begin{bmatrix}
    1 &  0 & 2 \\
    0 & -3 & -1\\
    0 &  1 & 1 \\
    \end{bmatrix}
    \to
    \begin{bmatrix}
    1 &  0 & 2 \\
    0 &  1 & 1 \\
    0 & -3 & -1\\
    \end{bmatrix}
    \to
    \begin{bmatrix}
    1 &  0 & 2 \\
    0 &  1 & 1 \\
    0 &  0 & 2 \\
    \end{bmatrix}
$$ 
>
> which should be sufficient to see that the collection spans $$\Bbb R^3$$.

2. Is the collection ...
> Yes for both. We represent the collection as a matrix and do some operations.
> $$
    \begin{bmatrix}
    1  & 10  & 2  \\
    4  & -3  & -6 \\
    0  &  1  & 1 \\
    \end{bmatrix}
    \to
    \begin{bmatrix}
    1  & 10  & 2  \\
    0  &  1  & 1 \\
    0  & -43 & -14 \\
    \end{bmatrix}
    \to
    \begin{bmatrix}
    1  & 10  & 2  \\
    0  &  1  & 1  \\
    0  & 0   & 29 \\
    \end{bmatrix}
$$
>
> We can see that the collection is linearly independent and is a basis for $$\Bbb R^3$$.

3. Multiply
> $$
    \begin{bmatrix}
    1 & 2 & 7 \\
    2 & 0 & 1 \\
    0 & 3 & -3\\
    \end{bmatrix}
    \pmatrix{10 \\ 0 \\ -2 }
    = \pmatrix{-4 \\ 18 \\ 6 }
$$

4. Let A = ... 
> We can see that A is the same collection in Q2 represented as columns, so:  
> a. Rank of A is 3.  
> b. Nullity of A is 0.  
> c. A _is_ invertible  
> d. det(A) $$\neq$$ 0

5. Find the change of basis from $$\mathcal B_1\text{ to }\mathcal B_2$$.
> To find the change of basis matrix S, we can set up the basis as columns of a matrix, which we could express as: 
> 
> $$
    \begin{align} 
    S \mathcal B_1     & = \mathcal B_2 \\
    (S \mathcal B_1^T) & = \mathcal B_2^T \\
    \mathcal B_1^T S^T & = \mathcal B_2^T \\
    \end{align} \\
    \text{We can setup the augmented matrix to find } S^T
$$
>
> $$
    \left[
    \begin{array}{ccc|ccc}
    1 & 2 & 0 & 1 & 1 & 1 \\
    1 & 0 & 1 & 2 & 0 & 2 \\
    1 & 0 & 3 & 0 & 3 & 3 \\
    \end{array}
    \right]
    \to 
    \left[
    \begin{array}{ccc|ccc}
    1 & 2 & 0 & 1 & 1 & 1 \\
    0 &-2 & 1 & 1 &-1 & 1 \\
    0 &-2 & 3 &-1 & 2 & 2 \\
    \end{array}
    \right]
    \to \\
    \left[
    \begin{array}{ccc|ccc}
    1 & 0 & 1 & 2 & 0 & 2 \\
    0 &-2 & 1 & 1 &-1 & 1 \\
    0 & 0 & 1 &-1 & \frac32 & \frac12 \\
    \end{array}
    \right]
    \to 
    \left[
    \begin{array}{ccc|ccc}
    1 & 0 & 0 & 3 & -\frac32 & \frac32 \\
    0 & 1 & 0 &-1 &\frac54 & -\frac14 \\
    0 & 0 & 1 &-1 & \frac32 & \frac12 \\
    \end{array}
    \right] \\
    \text{We have S:}\\
    \begin{bmatrix}
        3 & -1 & -1 \\
        -\frac32 & \frac54 & \frac32 \\
        \frac32 & -\frac14 & \frac12 \\
    \end{bmatrix}
$$

6. Vice versa from $$\mathcal B_2$$ to $$\mathcal B_1$$
> Doing the same calculations we have S for this case:
> $$
    \begin{bmatrix}
    \frac23 & \frac12 & -\frac16 \\
    2 & 2 & -2 \\
    -1 & -\frac12 & \frac32
    \end{bmatrix}
$$

### 2.2 Basic Questions

1. $$M = \pmatrix{2&3\\1&0}$$
>$$\text{Find eigenvalues and algebraic multiplicities}\\ 
    \begin{align}
    det(M-\lambda I)        & = 0 \\
    -\lambda(2-\lambda)-3   & = 0 \\
    \\
    \lambda = 3  \text{ or }  \lambda  &= -1
    \end{align}
$$
>
> For $$\lambda = 3$$:  
>> i. $$m_\lambda = 1 $$  
>> ii.   
>> $$
    \begin{align}
    (A-\lambda I)\vec x & = \vec0 \\
    \pmatrix{-1 & 3 \\ 1 & -3} \vec x & = \vec0 \\
    \vec x &= \pmatrix {3 \\ 1}
    \end{align}\\
    q_\lambda = 1
$$  
> 
>  
> For $$\lambda = -1$$:  
>> i. $$m_\lambda = 1 $$  
>> ii.   
>> $$
    \begin{align}
    (A-\lambda I)\vec x & = \vec0 \\
    \pmatrix{3 & 3 \\ 1 & 1} \vec x & = \vec0 \\
    \vec x &= \pmatrix {1 \\ -1}
    \end{align}\\
    q_\lambda = 1
$$ 
> 
> iii. Is diagonalizable ($$\forall m_\lambda : m_\lambda = q_\lambda$$)
> 

2. $$M = \pmatrix{1&1\\1&1}$$
>$$\text{Find eigenvalues and algebraic multiplicities}\\ 
    \begin{align}
    det(M-\lambda I)        & = 0 \\
    -1(1-\lambda)^2         & = 0 \\
    \\
    \lambda = 0  \text{ or }  \lambda  &= 2
    \end{align}
$$
>
> For $$\lambda = 0$$:  
>> i. $$m_\lambda = 1 $$  
>> ii.   
>> $$
    \begin{align}
    (A-\lambda I)\vec x & = \vec0 \\
    \pmatrix{1 & 1 \\ 1 & 1} \vec x & = \vec0 \\
    \vec x &= \pmatrix {1 \\ -1}
    \end{align}\\
    q_\lambda = 1
$$  
> 
>  
> For $$\lambda = 2$$:  
>> i. $$m_\lambda = 1 $$  
>> ii.   
>> $$
    \begin{align}
    (A-\lambda I)\vec x & = \vec0 \\
    \pmatrix{-1 & 1 \\ 1 & -1} \vec x & = \vec0 \\
    \vec x &= \pmatrix {1 \\ 1}
    \end{align}\\
    q_\lambda = 1
$$ 
> 
> iii. Is diagonalizable ($$\forall m_\lambda : m_\lambda = q_\lambda$$)
>

3. $$M = \pmatrix{1&0&0\\1&1&1\\0&1&0}$$
> i. After setting $$det(M-\lambda I) = 0$$, the eigenvalues are $$1, \frac12 + \frac{\sqrt{5}}{2}, \frac12 - \frac{\sqrt{5}}{2}$$ all with $$m_\lambda = 1$$
>   
> For $$\lambda = 1$$
>> Setting $$(M-I)\vec x = 0 $$ yields $$\vec x = c\pmatrix{-1\\1\\1} (q_\lambda = 1)$$  
>
> For $$\lambda = \frac12 - \frac{\sqrt5}2$$
>> The eigenvectors are: $$c\pmatrix{0\\-\frac{\sqrt5}2+\frac12\\1}$$  
>
> For $$\lambda = \frac12 + \frac{\sqrt5}2$$
>> The eigenvectors are: $$c\pmatrix{0\\\frac{\sqrt5}2+\frac12\\1}$$

4. $$M = \pmatrix{0&1&2\\0&0&3\\0&0&0}$$
> i. We find that $$\lambda = 0$$ with $$m_\lambda=3$$  
> ii. The one eigenvector is $$\pmatrix{1\\0\\0} (q_\lambda = 1)$$  
> iii. It is defective because one of $$q_\lambda < m_\lambda$$  
> iv. Defective.  

### 2.3 Definition Questions

1. Given A ...   
> a. det(A) = 0? No. If det(A - 0I) = 0, it follows 0 is an eigenvector, but since A is 3 &times; 3 and the algebraic multiplicity of $$\lambda_{-17}$$ is 3, 0 can't be an eigenvalue.
> 
> b. Nullity of A: 0
> 
> c. Rank of (A + 17I): 2 (by definition of geometric multiplicity)
> 
> d. Nullity of (A + 17I): 1 (by definition of geometric multiplicity)
> 
> e. Free variables in RREF for (A + 17I): 1 (from d.)
> 
> f. Leading variables in RREF for A: 3 (from b.)
> 
> g. det(A + 17I) = 0 (because -17 is eigenvalue)
> 
> h. $$det(A^2(A + 17I)) = 0 $$ (because det(AB) = det(A)det(B), from g.)

### 2.4 Challenge Questions

1. Let A = $$ \pmatrix{a&b\\c&d} $$
> a. Characteristic equation: $$(a-\lambda)(d-\lambda)-bc = 0$$
> 
> b. $$\frac{(a+d)\pm\sqrt{(a-d)^2+4(ad-bc)}}{2} = \lambda$$
> 
> c. $$(a-d)^2 + 4(ad-bc) \neq 0 $$
> 
> d. $$(a-d)^2 + 4(ad-bc) = 0 $$
> 
> e. $$(a-d)^2 + 4(ad-bc) < 0 $$
> 

2. Prove eigenspace of an eigenvalue of a matrix is a vector space from definitions.
> Stuff
