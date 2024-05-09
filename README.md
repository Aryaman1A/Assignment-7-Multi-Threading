# Assignment-7-Multi-Threading
# Introduction
This Python endeavor delves into multithreading within the language, specifically applying it to matrix multiplication. Matrix multiplication poses a computationally demanding task, particularly with sizable matrices. Leveraging multithreading, the aim is to parallelize this process, potentially curtailing overall execution time.

# Prerequisites

Python 3.x
NumPy
Matplotlib (for visualization)
Project Structure

multi_threading.py: Houses the main script for executing multithreaded matrix multiplication and performance analysis.
matrices.py: A module for generating random matrices for multiplication.
README.md: Documentation offering an overview of the project, instructions, and analysis.
# Approach
Matrix Generation: The matrices module generates a collection of random matrices with dimensions (1000, 1000) using NumPy's randint() function. These matrices serve as input for the multiplication task.

Matrix Multiplication Function: The matrix_multiplication() function executes matrix multiplication utilizing NumPy's dot() function.

Multithreading: The multiplication_task() function embodies the matrix multiplication task for a subset of matrices. The total matrices are divided into chunks, with each chunk allocated to a separate thread for concurrent execution.

Thread Management: The run_threads() function initiates and launches multiple threads, with each tasked with handling a matrix multiplication chunk. Upon completion of all thread tasks, the function computes and returns the total execution time.

# Analysis
Performance assessment of multithreading involves varying the thread count from 1 to 15. For each configuration, execution time is measured, and a graph is plotted illustrating the correlation between thread count and time taken.

# Results
Execution time diminishes as the thread count escalates, up to a certain threshold. Beyond this point, further thread additions may not yield enhancements and could potentially degrade performance due to overhead. The optimum thread count hinges on factors like available CPU cores and computation nature.

# Conclusion
Multithreading proves instrumental in bolstering the performance of computationally intensive tasks such as matrix multiplication, optimizing resource utilization. Nonetheless, achieving optimal results necessitates meticulous consideration of factors like load balancing, overhead, and synchronization.
