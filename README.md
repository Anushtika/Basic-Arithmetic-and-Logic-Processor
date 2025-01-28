# Basic-Arithmetic-and-Logic-Processor
class SimpleProcessor:
def __init__(self):
self.registers = [0] * 8 # 8 general-purpose registers
self.result = 0
def add(self, reg_a, reg_b):
self.result = self.registers[reg_a] + self.registers[reg_b]
def subtract(self, reg_a, reg_b):
self.result = self.registers[reg_a] - self.registers[reg_b]
def multiply(self, reg_a, reg_b):
self.result = self.registers[reg_a] * self.registers[reg_b]
def divide(self, reg_a, reg_b):
if self.registers[reg_b] != 0:
self.result = self.registers[reg_a] // self.registers[reg_b]
else:
print("Error: Division by zero!")
def logic_and(self, reg_a, reg_b):
self.result = self.registers[reg_a] & self.registers[reg_b]
def logic_or(self, reg_a, reg_b):
self.result = self.registers[reg_a] | self.registers[reg_b]
def logic_not(self, reg_a):
self.result = ~self.registers[reg_a]

# Example usage
processor = SimpleProcessor()
processor.registers[0] = 5
processor.registers[1] = 3
processor.add(0, 1)
print("Addition Result:", processor.result) # Output: 8
processor.subtract(0, 1)
print("Subtraction Result:", processor.result) # Output: 2
processor.multiply(0, 1)
print("Multiplication Result:", processor.result) # Output: 15
processor.divide(0, 1)
print("Division Result:", processor.result) # Output: 1 (integer division)
processor.logic_and(0, 1)
print("Logical AND Result:", processor.result) # Output: 1 (binary 0101 & 0011 = 0001)
processor.logic_or(0, 1)
print("Logical OR Result:", processor.result) # Output: 7 (binary 0101 | 0011 = 0111)
processor.logic_not(0)
print("Logical NOT Result:", processor.result) # Output: -6 (binary ~0101 = 11111010 in
two's complement)
