# Iterative Linear Solvers

This repository is dedicated to the implementation of iterative methods for solving systems of linear equations, developed as part of the **Numerical Analysis** (Numerical Methods) curriculum at the **University of Antioquia**.

## Project Status: Under Active Development

**Please note:** This project has just begun!

I am currently setting up the structure and environment. Over the next few weeks, I will be writing the source code and documenting each step. 

### Planned Features & Methods:
* **Jacobi Method** (Matrix-based iteration)
* **Gauss-Seidel Method**
* **JOR** (Jacobi Over-Relaxation)
* **BSOR** (Block Successive Over-Relaxation)

---

### 🇨🇴 Nota en Español
Este repositorio está en **desarrollo activo**. Actualmente me encuentro configurando la estructura inicial del proyecto para la materia de Métodos Numéricos en la UdeA. Todo el código, las matrices de iteración y la documentación detallada se irán subiendo progresivamente.

## Mathematical Formulation

The project focuses on matrix-based implementations rather than purely algebraic loops. For a linear system $Ax = b$, the matrix $A$ is decomposed into its diagonal $D$, strictly lower $A_L$, and strictly upper $A_R$ parts such that $A = D + A_L + A_R$.

### 1. Jacobi Method
The solver initializes by decoupling the system using the **Jacobi iteration matrix** $B_j$ and the modified constant vector $c_j$:

$$ B_j = -D^{-1}(A_L + A_R)$$

$$ c_j = D^{-1}b $$

The system is then solved iteratively by updating the solution vector $x$ at each step $n$:

$$ x^{(n+1)} = B_j x^{(n)} + c_j $$

Where `@` (matrix multiplication).
