def f(x):
  return x**5 -2*x**2 -3



def LinInt(f,A,B,eps, max_iter):
  #initial checks before (edge cases), the function is ran
  # A should be less than B
  # and f(A) x f(B) < 0 ( this check enures that f(A) and f(B) have opposite signs)
  counter = 0
  if A>=B or (f(A)*f(B) >= 0):
    raise ValueError("A needs to be less than B such that f(A) and f(B) have opposite signs")
  if A<B and (f(A)*f(B) < 0):
    #print statement to check its working
    print(f"A: {A}, B{B}, f(A): {f(A)}, f(B): {f(B)}, the tolerance is: {eps}, Number of Iterations is: {max_iter}")
    # iteration

    initial_x = A
    while counter < max_iter:
      x_next = (A * f(B) - B * f(A)) / (f(B) - f(A))

      print(f"Iteration number: {counter + 1 }: x_next = {x_next}")


      if abs(x_next-initial_x) < eps:
        return x_next

      if (f(A) * f(x_next)) < 0:
        A = x_next
      else:
        B = x_next

      initial_x = x_next
      counter += 1

    raise ValueError("Maximum Iterations however convergence wasnt reached.")


result = LinInt(f=f,A=1,B=2,eps = 1e-6, max_iter = 1_000_000)
print(f"Final result: {result}")




# Same equation - New Method
# f(x) = x^5 -2x^2 -3 = 0

#  A and B are such that A < B and f(A) & f(B) have opposite signs

#  x (n) = (A(n) x f(B(n)) - (B(n) x f(A(n)) / f(B(n)) - f(A(n))
# n = 1

# f(x1) is evaluated and then the formula is repeated
#       after replacing either A1 or B1 with x1, basded on whether f(x1) has the same sign as either f(A1) ir f(B1)
