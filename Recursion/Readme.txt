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
