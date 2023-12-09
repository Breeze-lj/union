# C++11面试填空题（2023版）

### 1. C++11中____可以用于定义常量表达式,在编译期计算。​

答案:constexpr​
```
constexpr 是 C++ 中的一个关键字，用于指示一个变量、函数或类成员是编译时常量。这意味着在编译时，编译器会检查这些常量，并在编译期间计算它们的值。这在编译时检查代码的正确性非常有用，因为它可以防止在运行时出现未定义的行为。

在 C++20 标准中，constexpr 还具有以下特性：
                    可以在声明时初始化。
                    可以在编译时计算。
                    可以用于声明函数，并且这些函数可以在编译时计算返回值。​
```
### 2. 使用C++11的范围for循环遍历数组,填空处应该填写什么:​
int arr[] = {1, 2, 3};​​<br />
for(______) {​​<br />
std::cout << x << std::endl; ​​<br />
}​​<br />

答案:auto x:arr / int x:arr/auto x : arr / int x : arr​​<br />

### 3. 使用C++11的委托构造函数,填空处应该填写什么:​
class Person {​​<br />
public:​​<br />
Person(string name) {​​<br />
this->name = name; ​​<br />
}​​<br />
​
Person(string name, int age) : ______ {​<br />
this->age = age;​}​​<br />
​
private:​​<br />
string name;​​<br />
int age;​​<br />
};​​<br />

答案：Person(name) ​​<br />

### 4. 使用C++11的继承构造函数,填空处应该填写什么:​
struct B : A {​​<br />
using A::A; // 使用继承构造函数​​<br />
B(int x) : ______ {​​<br />
​
}​​<br />
};​​<br />

答案:A(x)​​<br />

### 5. 使用C++11的lambda表达式语法,填空处应该填写什么（x,y均为int类型）:​
auto func = ______ {​​<br />
return x + y; ​​<br />
};​​<br />

答案:[](int x, int y)​​<br />

### 6. 使用C++11的显式虚函数重载,填空处应该填写什么:​
struct A {​​<br />
virtual void func() ______;​​<br />
};​​<br />

答案:override​​<br />

### 7. ____是C++中实现运行时多态的关键。

​答案:虚函数 / virtual​​<br />
​
### 8. 在C++中,____使得基类指针可以安全地转换为派生类指针。 ​

答案:dynamic_cast / 动态类型转换​​<br />

### 9. C++中引入____是为了使动态分配的数组能够自动释放内存。 ​

答案:智能指针 / smart pointer​​<br />
​
### 10. C++11中 std::____用于将任意参数打包成一个类型。​

答案:tuple​​<br />
std::tuple 是一个模板类，可以存储任意类型的数据，包括整数、浮点数、对象等。<br />
以下是一个使用 std::tuple 的简单示例：<br />
```
#include <iostream>
#include <tuple>

int main() {
  auto my_tuple = std::make_tuple(1, 2.0, "hello");

  // 访问第一个元素
  std::cout << std::get<0>(my_tuple) << std::endl;  // 输出：1

  // 访问第二个元素
  std::cout << std::get<1>(my_tuple) << std::endl;  // 输出：2.0

  // 访问第三个元素
  std::cout << std::get<2>(my_tuple) << std::endl;  // 输出：hello

  return 0;
}
```