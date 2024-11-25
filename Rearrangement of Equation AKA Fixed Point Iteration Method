#Equation to solve:

#   f(x) = x^5 -2x^2 -3 = 0
#   Rearranged:
#   x= (2x^2 +3)**1/5     This is phi


def phi(x):
  return (2*x**2 + 3) ** (1/5)

# fpa = Fixed Point Iteration
# input parameters:
# phi = rearranged function
# x0 = initial guess
# tol = tolerance between successive iteration ( |x (sub n+1) - x(n) |)
# max_iter = maximum inumber of iterations to prevent infite loops if divergence occurs


# The for loop:
# runs until solution is found or number of max iterations is reached.
# checks the abs value of the return of the phi function, each iteration, in theory, should lower the value less than the tolerance

def fpa(phi, x0, tol, max_iter):
  x = x0

  for i in range(max_iter):
    x_next = phi(x)
    print(f"Iteration {i+1}: x = {x_next}")
    if abs(x_next - x) < tol:
      return x_next
    x = x_next

  print("No convergence")
  return None



# Initialisation of the input parameters
# x0, tol, and max iterations

x0 = 3
tol = 1e-6
max_iterations = 1000

root = fpa(phi, x0 = x0, tol = tol, max_iter = max_iterations)
if root is not None:
  print(f"Root found: x = {root}")
