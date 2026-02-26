# CEL-CASESTUDY
Case Study: Dominant Eigenvalue Using Power Method
Name: Shubham Sharma
Roll Number: 23BME064
Course: Computational Engineering Laboratory (20ME331T)
Semester: VI
Branch: Mechanical Engineering
Academic Year: 2025–26

1. Objective
To determine the dominant eigenvalue and corresponding eigenvector of a given square matrix using the Power Method in MATLAB.

2. Theory
Eigenvalues were obtained using the characteristic equation:
[A]{X}=λ{X}

which leads to:
det⁡([A]-λ[I])=0

Solving this determinant gives a polynomial whose roots are eigenvalues.
However, for large matrices, solving the characteristic polynomial becomes computationally intensive. Therefore, numerical iterative methods such as the Power Method are used to compute the dominant eigenvalue efficiently.

Power Method Concept
If a matrix has eigenvalues:
∣λ_1∣>∣λ_2∣>∣λ_3∣...

Then repeated multiplication of any non-zero initial vector by matrix Agradually aligns the vector in the direction of the eigenvector corresponding to λ_1.
This principle forms the basis of the Power Method.

3. Mathematical Formulation
Given matrix:
A=[■(0&2&3@1&1&1@0&2&9)]

Initial vector:
v=[█(1@1@1)]

Tolerance:
10^(-6)


Iterative Steps
	v=A⋅v
	λ=max⁡(∣v∣)
	Normalize: v=v/λ
	Compute error: ∣λ-λ_old∣
	Repeat until error < tolerance

4. Algorithm
START
Initialize:
Matrix A
Initial vector v=[1;1;1]
Tolerance = 10^(-6)
Error = 1
Previous eigenvalue = 0
WHILE (error > tolerance)
	Multiply: v=A⋅v
	Extract largest component
	Normalize vector
	Calculate difference between new and old eigenvalue
	Update previous value
END WHILE
Display eigenvalue and eigenvector
STOP

5. MATLAB Code
 


6. Results
Parameter	Value
Dominant Eigenvalue	9.325883
Corresponding Eigenvector	[0.35, 0.16, 1.00]

7. Discussion
The dominant eigenvalue obtained is:
λ=9.325883

This value represents the largest scaling factor of matrix A.
The corresponding eigenvector:
[█(0.35@0.16@1.00)]

indicates that the third component has the strongest contribution in the dominant direction.
The decreasing error confirms convergence of the method.

8. Conclusion
This case study successfully demonstrates the use of the Power Method to compute the dominant eigenvalue of a matrix.
Compared to solving the characteristic equation, the iterative approach:
	Is simpler to implement
	Requires less computational effort
	Converges efficiently when one eigenvalue dominates
The experiment validates the importance of numerical methods in solving engineering problems involving eigenvalue analysis.

