```mermaid
classDiagram
class Calculator {
+ Summ(a: int, b: int): int
+ Difference(a: int, b: int): int
+ Multiplication(a: int, b: int): int
+ Degree(a: int, b: int): int
}

class User {
- Name: string
+ User(name: string)
+ UseCalculator(calc: Calculator, num1: double, num2: double): void
}

class History {
- calculations: List<string>
+ AddCalculation(calculation: string): void
+ DisplayHistory(): void
}

class Logging {
+ LogOperation(user: string, operation: string): void
}


User  -->  Calculator : uses
Calculator  -->  History : has
Calculator  -->  Logging : uses
```
