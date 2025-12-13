# huffman-coding
A python tool for computing and visualizing the Huffman coding algorithm. Given a list of probabilities 0 < p < 1 such that &Sigma; p = 1, computes the iterations of the Huffman algorithm and displays the tree converging to the final value of 1.0.

## Present work
In the current notebook, an example using the Dirichlet distrubution is given, randomly drawing *n* probabilities that sum to 1. The graph produced demonstrates the descending ordering and the summing of the two lowest probabilities, repeating until the final two probabilities sum to the convergent value 1.

An issue observed with the method used is that the sum of the two least probabilities in any given iteration may not draw edges to that sum in the next iteration. This is a result of rounding error/design and can be resolved by adjusting the rounding design and tolerance.

## Next steps
The next part of the project is to correctly track the path of each probability event across the tree with binary digits, and produce the final codebook. At each iteration of the algorithm, only the current least probabilities need to be tracked and labeled with a digit. Ideally, these digits would be displayed upon the tree branch.
