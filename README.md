# Steffen
import math


# to compute the solution we use binomial distribution  reflecting to the binomial model

def binomial(n, k):
    assert 0 <= k <= n
    return math.factorial(n) // (math.factorial(k) * math.factorial(n - k))

# And there is were we get the size of the actual grid

print("Welcome to this simple calculator. First of all I need to know the horizontal length of the grid")
a = int(input())

print("Now I need the vertical length of the grid")
b = int(input())

# from the top left corner to the bottom right corner in case of an A * B grid it takes A times B moves we know that
# n =a +  b and k = (a + b)/2
n = a + b
k = (a + b) / 2


def move():
    return str(binomial(n, k))


print(move())
