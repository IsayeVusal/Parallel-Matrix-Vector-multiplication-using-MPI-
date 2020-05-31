# Parallel-Matrix-Vector-multiplication-using-MPI

Implementing parallel matrix vector multiplication using MPI point-to-point communication i.e. Send
and Recv. How the matrix and vectors are divided (distributed)
among workers, what is shared among them, how is the work distributed, what individual worker will
do and what master worker will do.

I want to mention that in the process of matrix-vector multiplication the number of computational operations for computing the inner product is the same for all the basic subtasks. Therefore, in case when the number of processors p is less than the number of basic subtasks m, we can combine the basic subtasks in such a way that each processor would execute
several of these tasks. In this case each subtask will hold a row stripe of the matrix A After completing
computations, each aggregated basic subtask determines several elements of the result vector c. 
