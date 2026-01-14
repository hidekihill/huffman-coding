# huffman-coding
A python tool for computing and visualizing the Huffman coding algorithm. Given the discrete probability events of a probability density function, computes the iterations of the Huffman algorithm and displays the tree converging to the final value of 1.0. Note that the the tool requries the discrete probabilites to sum to 1.0 as requried in the probability space axioms.

## Present work
In the current notebook, several examples are given: one example using the Dirichlet distrubution randomly draws *n* probabilities (again, subject to the constraint that they sum to 1). The graph produced demonstrates the descending ordering and the summing of the least two probabilities, repeating until the final two probabilities sum to the convergent value of 1. The following figure illustrates an example:

<img width="600" height="350" alt="image" src="https://github.com/user-attachments/assets/6c12e349-5373-4acc-b5ff-678860c78aa0" />

An issue observed with the method used is that the sum of the two least probabilities in any given iteration may not draw edges to that sum in the next iteration. This is a result of rounding error/design and can be resolved by adjusting the rounding design and tolerance. Another fault arises when the final probability in the tree is not 1; the final node should always be 1. This is also the result of rounding errors despite the assertion that probabilities sum to 1. The following figure illustrates these rounding errors:

<img width="600" height="350" alt="image" src="https://github.com/user-attachments/assets/e7c4dcc8-5ee8-4850-82db-83773d87e6ea" />


## Next steps
The next part of the project is to correctly track the path of each probability event across the tree with binary digits, and produce the final codebook. At each iteration of the algorithm, only the current least probabilities need to be tracked and labeled with a digit. Ideally, these digits would be displayed upon the tree branch.
