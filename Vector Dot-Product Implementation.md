# **Vector Dot-Product Implementation**

## **Introduction**
>The dot product is one way of multiplying two or more vectors. The resultant of the dot product of vectors is a scalar quantity. Thus, the dot product is also known as a scalar product. Algebraically, it is the sum of the products of the corresponding entries of two sequences of numbers.

## **Definition**
In vector algebra, if two vectors are given as: 
**A = [a₁, a₂, ..., aₙ]**
**B = [b₁, b₂, ..., bₙ]**

**Vector Dot Product**
`a · b = a₁b₁ + a₂b₂ + ... + aₙbₙ`

![Dot product image](https://media.geeksforgeeks.org/wp-content/uploads/20240515223425/dot.webp)

## **Implementation in C++**
```
#include <iostream>
#include <vector>
using namespace std;

int dotproduct(vector<int> &arr1, vector<int> &arr2){
    int product= 0;
    for(int i= 0; i< arr1.size(); i++){
        product+= arr1[i]*arr2[i];
    }
    return product;
}

int main(){
    vector<int> arr1= {3,4,5};
    vector<int> arr2= {7,8,9};
    if(arr1.size() != arr2.size()){
        cout<<"The vectors are unequal in size"<<endl;
    }
    else{
        cout<<"The dot product is "<<dotproduct(arr1, arr1)<<endl;
    }
    return 0;
}
```
## **Properties of Dot Product**
+ **Commutative**: a.b = b.a
+ **Distributive**: a.(b+c) = a.b + a.c
+ **Associative with scalar multiplication**: k(a.b) = (ka).b = a.(kb)
### Two Types of Products: 
1. Dot Product
    + Gives scalar output
2. Cross Product
    + Gives vector output
### Checklist:
- [x] Dot product of two vectors
- [ ] Cross product of two vectors
## Footnote
Dot product[^1].
Cross product[^2].

[^1]: The scalar product is calculated as the product of magnitudes of a, b, and cosine of the angle between these vectors.
[^2]: The Vector product of two vectors, a and b, is denoted by a × b. Its resultant vector is perpendicular to a and b.
## Alerts
>[!Caution]
>Make sure the values aren't negative.
## Versions of Algorithms
|Version|Approach|Complexity|
|----|----|----|
|Naive|	Basic for-loop|	𝑂(𝑛)|
|Parallelized|	Multithreading|O(n/p)|

If you need further information, [click here](https://www.geeksforgeeks.org/dot-product/).



