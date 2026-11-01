# SOLID Principles 

SOLID Principles are one of the most important design principles which helps developers manage most of the software desgin problems.
These SOLID Principles are introduced by Robert C. Martin, an american software engineer known for his promotions of some great software design principles.
The term SOLID is an acronym (an abbreviation formed from parts of words) for five design principles that one should follow to make software designs more understandable, flexible and maintainable.

SOLID Stands for:
1.S-Single Responsibility Principle(SRP)
2.O-Open/Closed principle(OCP)
3.L-Liskov Substitution Principle(LSP)
4.I-Interface Segregation Principle(ISP)
5.D-Dependency Inversion Principle(DIP)

The main goal of these principles is to reduce code complexity and make software easier to modify, test and maintain for long term.

## 1.Single Responsibility Principle:
This principle states that **A class should have one and only one reason to change, meaning that a class should have only one job**.
Each class should have their own tasks instead of doing multiple things that are unrelated.

Example:
          class Employee {
              void calculateSalary() {
                  System.out.println("Calculating salary");
              }
          }
          
          class EmployeeReport {
              void generateReport() {
                  System.out.println("Generating report");
              }
          }

Here, salary calculation and report generation are handled by seperate classes.
This helps us in making code easier to manage and modify.

## 2.Open/Closed Principle:
This principle tells us that **Objects or entities should be open for extension but closed for modification.**
We should be able to add new features without changing existing working code.

Example:
          interface Payment {
              void pay();
          }
          
          class UpiPayment implements Payment {
              public void pay() {
                  System.out.println("UPI payment");
              }
          }
          
          class CardPayment implements Payment {
              public void pay() {
                  System.out.println("Card payment");
              }
          }

Here, we can also add another payment method by creating a new class without changing the existing classes.
This helps us in adding new features easier.

## 3.Liskov Substitution Principle:
This principle tells us that **one must be able to replace a superclass object with a subclass object without affecting the correctness of the program.**
A child class should follow the expected behaviour of its parent class.

Example:
          class Bird {
              void eat() {
                  System.out.println("Bird is eating");
              }
          }
          
          class FlyingBird extends Bird {
              void fly() {
                  System.out.println("Bird is flying");
              }
          }
          
          class Sparrow extends FlyingBird {
          }
          
          class Penguin extends Bird {
          }

Here, Sparrow can fly, but Penguin cannot. So, we keep flying behaviour in a seperate class instead of forcing every bird to implement it.
This helps us in avoiding unexpected changes and behaviour when using inheritance.


