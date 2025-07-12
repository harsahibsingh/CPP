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
