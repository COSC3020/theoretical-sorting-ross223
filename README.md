[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

As we know from class, the theoretical worst case scenerio of any 
comparison-based algorithm that assumes only two elements are being 
compared at any one time is at least $\Omega (nlogn)$. Therefore, any 
claims of an algorithm that has runtime of O(n) is almost certainly
untrue.

To verify this claim I would generate a couple different arrays to 
sort of different lengths:
1. An array that is already sorted
2. An array that is reverse sorted
3. An array that is completely random
4. An array that uses multiple of the same elements (Ex: [1, 0, 0, 1])
5. An array that is empty

Since these arrays being tested provide a wide range of scenerios sorting 
algorithms need to account for, I would say they create a good testing 
environment.

For any of these given arrays, the algorithm must be able to sort the array
linearly proportional to the size of the array. Therefore, using some sort
of timing software would be beneficial for the testing process. Additionaly, 
testing the algorithm in a controlled environment would be essential, so 
every test would be done as similarly as possible to account for this. 

Once that I have finished timing I would graph the time vs number of elements 
plot and analyze if it follows linear growth. If it does then I would attempt to 
try more arrays of before finishing my analysis.

If any of these arrays fail to sort properly or the algorithm seems to follow
a different pattern of growth then I would assume that the algorithm is 
either faulty or does not have a time complexity of O(n).

If these tests prove to work properly I would be very suprised and the
algorithm would change the world of sorting forever, but more than
likely they will fail, proving that the algorithm does not have time 
complexity of O(n) and the researcher is incorrect in their assesment.
