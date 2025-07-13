Recursion: A way to write a program where a function calls itself

1. Direct Recursion:

void fun1()
{
  fun1();
}

2. Indirect Recursion:

void fun2()
{
  fun1();
}

void fun1()
{
  fun2();
}

Base Case: Recursion terminating conditions

Typical Structure Of Recursive Function:

returnType func(parameters)
{
  Base Case;

  Some Code;

  Recursive call to the func;(with change of parameter passed)

}

Note: Any program that is programmed using iteration can be progrmmed using recursion.(and vice-versa)

Applications Of Recursion:

1. Algorithms based on recursion include:
      Dynamic Programming
      Backtracking
      Divide and Conquer(Binary Search, Quick Sort , Merge Sort)

2. Problems inherently recursive:
      Tower Of Hanoi
      DFS based traversals (DFS of graph and Inorder/Preorder/Postorder traversal of tree )

Note:
Iterative Solutions causes lesser overheads
Ex: Recursive Binary Search : O(logn) Aux space
    Iterative Binary Search : O(1) Aux space
One more problem with recurssion is function call overhead
Still recursion is used because of ease in implementation

Tail Recursive :
When parent function has nothing to do when child function finishes i.e in function recursive call happens at last (nothing happens after that)
Tail recursive functions takes less time in modern compilers wrt non-tail recursive function.

Ex: a tail recursive function:

void func(int n)
{
  if(n ==0)
    return ;

  print (n);
  func(n-1);  //recursion at last
}

A modern compiler do following changes to it:

void func(int n)
{
start:
  if(n ==0)
    return ;

  print (n);
  func(n-1);  -> n=n-1;
                 goto start; 
}
//i.e above recursion is removed completely, this way aux space need to store state of caller while calling recursion, also need to resume all the states , all this overhead is gone.
//These changes which modern compilers do are called Tail call elimination.

Note: All non-tail recursive functions cannot be converetd to til recursive



