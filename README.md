# Delinquency-Calulator-
Input your branch's percentages to find how much money you need to move/collect. Current and goal percentages depend on what category you want to calculate. For example, if you want to know how much money you need to move from the accounts that are 30-days-late, focus only on the '30' category. Also, the total ledger changes hourly, so use the total ledger at the time of the calculation. The total ledger is the total value of the branch with all of its accounts. Every category percentage and the total ledger can be found on the branch statistical summary report. The goal percentages are given at the beginning of the month to all staff. 

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
