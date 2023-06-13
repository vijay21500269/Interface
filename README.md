# Interface

## Aim:
To write a C# program using interface concept



## Algorithm:
Step 1:
Create an interface.

Step 2:
Create a child class.

Step 3:
Declare 2 functions deposit() and withdrawal() as abstract methods in the interface.

Step 4:
Create those 2 functions in the child class and perform respective operation.

Step 5:
Use while loop and and switch case to Get the choice from the user whether to perform withdrawal or deposit operation.

Step 6:
After performing the functions display the remaining balance of the use

## Program:
~~~
Developed by: Vijay R
Register Number: 212221230121
~~~
~~~
using System;
namespace ex09
{
    public interface bank
    {
        void deposit(int amt);
        void withdraw(int amt);
    }
    public class accnt : bank
    {
        public int balance = 50600, amt;
        int a = 1;
        public accnt()
        {

            while (a == 1)
            {
                Console.WriteLine("Enter 1 to deposit and 2 to withdraw and 3 to display your balance:");
                int choice = Convert.ToInt32(Console.ReadLine());
                Console.WriteLine();
                switch (choice)
                {
                    case 1:
                        Console.WriteLine("Enter the amount to deposit");
                        amt = Convert.ToInt32(Console.ReadLine());
                        Console.WriteLine();
                        deposit(amt);
                        break;

                    case 2:
                        Console.WriteLine("Enter the amount to be withdrawn");
                        amt = Convert.ToInt32(Console.ReadLine());
                        Console.WriteLine();
                        withdraw(amt);
                        break;

                    case 3:
                        display();
                        break;
                }
            }
            Console.ReadKey();

        }
        public void deposit(int amt)
        {
            balance += amt;
        }
        public void withdraw(int amt)
        {
            balance -= amt;
        }
        public void display()
        {
            Console.WriteLine("Your remaining balance is " + balance);
            a = 0;
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            accnt p1 = new accnt();
        }
    }
}
~~~

## Output:
![Exp9](https://github.com/vijay21500269/Interface/assets/94381788/99967637-ec9f-41a8-bc7c-22005d558077)


## Result:
Thus, C# program to develop a bank application using interface is implemented successfully.

