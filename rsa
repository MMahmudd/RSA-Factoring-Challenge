#!/usr/bin/python3

import sys
from sympy import factorint

def factorize_rsa_number(n):
    factors = factorint(n)
    return factors.items()

def factorize_file(filename):
    with open(filename, 'r') as file:
        number = int(file.read().strip())
        factors = factorize_rsa_number(number)
        for factor, exponent in factors:
            print(f"{number}={factor}^{exponent}")

if __name__ == '__main__':
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
        sys.exit(1)

    filename = sys.argv[1]
    factorize_file(filename)
