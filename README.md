# Delinquency-Calulator-
Input your branch's percentages to find how much money you need to move 

import sympy 
from sympy import symbols
from sympy.solvers import solve 

x = symbols('x') #What percentage you're at.
y = symbols('y') #Goal or where you need to be. 
t = symbols('t') #Total ledger.
a = symbols('a') #Final answer.

#input your values below. Note that the total ledger changes hourly. 
x = 0.035
y = 0.03
t = 5678234

eq = ((x-y)*t) - a

print("a = ", solve(eq,a))
