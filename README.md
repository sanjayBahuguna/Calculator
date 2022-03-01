# Calculator

def add(n1, n2):
  return n1 + n2
def sub(n1, n2):
  return n1 - n2
def multiply(n1, n2):
  return n1 * n2
def divide(n1, n2):
  return n1 / n2

all = {"+": add,
"-": sub,
"*": multiply,
"/": divide}
def calculator():
  first = float(input("what is your number?" ))
  for n in all:
    print(n)
  should_con = True
  while should_con:
    OP = input("pick one of the caculation from the above.")
    second = float(input("what is second your number?" ))
    cacl = all[OP]
    ans = cacl(first, second)
    print(f"{first} {OP} {second} = {ans}")
  
    if input("you want to continue with same asnwer pree 'y' or pree'n' to new calculation. ") == "y":
      first = ans
    else:
      should_con = False
      calculator()

calculator()

  

  
  
