---
title: "Structured Exception Handling (C-C++)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: language-reference
H1: Structured Exception Handling (C/C++)
ms.assetid: dd3b647d-c269-43a8-aab9-ad1458712976
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Structured Exception Handling (C-C++)
Although Windows and Visual C++ support structured exception handling (SEH), we recommend that you use ISO-standard C++ exception handling because it makes code more portable and flexible. Nevertheless, in existing code or for particular kinds of programs, you still might have to use SEH.  
  
## Microsoft Specific  
  
## Grammar  
 *try-except-statement* :  
  
 `__try` *compound-statement*  
  
 `__except` ( `expression` ) *compound-statement*  
  
## Remarks  
 With SEH, you can ensure that resources such as memory blocks and files are correctly if execution unexpectedly terminates. You can also handle specific problems—for example, insufficient memory—by using concise structured code that does not rely on `goto` statements or elaborate testing of return codes.  
  
 The try-except and try-finally statements referred to in this article are Microsoft extensions to the C language. They support SEH by enabling applications to gain control of a program after events that would otherwise terminate execution. Although SEH works with C++ source files, it's not specifically designed for C++. If you use SEH in a C++ program that you compile by using the [/EH](../vs140/-EH--Exception-Handling-Model-.md) option—together with certain modifiers—destructors for local objects are called but other execution behavior might not be what you expect. (For an illustration, see the example later in this article.) In most cases, instead of SEH we recommend that you use ISO-standard [C++ exception handling](../vs140/try--throw--and-catch-Statements--C---.md), which Visual C++ also supports. By using C++ exception handling, you can ensure that your code is more portable, and you can handle exceptions of any type.  
  
 If you have C modules that use SEH, you can mix them with C++ modules that use C++ exception handling. For information, see [Exception Handling Differences](../vs140/Exception-Handling-Differences.md).  
  
 There are two SEH mechanisms:  
  
-   [Exception handlers](../vs140/Writing-an-Exception-Handler.md), which can respond to or dismiss the exception.  
  
-   [Termination handlers](../vs140/Writing-a-Termination-Handler.md), which are called when an exception causes termination in a block of code.  
  
 These two kinds of handlers are distinct, but are closely related through a process known as "unwinding the stack." When an exception occurs, Windows looks for the most recently installed exception handler that is currently active. The handler can do one of three things:  
  
-   Fail to recognize the exception and pass control to other handlers.  
  
-   Recognize the exception but dismiss it.  
  
-   Recognize the exception and handle it.  
  
 The exception handler that recognizes the exception may not be in the function that was running when the exception occurred. In some cases, it may be in a function much higher on the stack. The currently running function and all other functions on the stack frame are terminated. During this process, the stack is "unwound;" that is, local variables of terminated functions—unless they are `static`—are cleared from the stack.  
  
 As it unwinds the stack, the operating system calls any termination handlers that you've written for each function. By using a termination handler, you can clean up resources that otherwise would remain open because of an abnormal termination. If you've entered a critical section, you can exit in the termination handler. If the program is going to shut down, you can perform other housekeeping tasks such as closing and removing temporary files.  
  
 For more information, see:  
  
-   [Writing an Exception Handler](../vs140/Writing-an-Exception-Handler.md)  
  
-   [Writing a Termination Handler](../vs140/Writing-a-Termination-Handler.md)  
  
-   [Using Structured Exception Handling with C++](../vs140/Using-Structured-Exception-Handling-with-C--.md)  
  
## Example  
 As stated earlier, destructors for local objects are called if you use SEH in a C++ program and compile it by using the **/EH** option with certain modifiers—for example, **/EHsc** and **/EHa**. However, the behavior during execution may not be what you expect if you are also using C++ exceptions. The following example demonstrates these behavioral differences.  
  
```cpp  
#include <stdio.h>  
#include <Windows.h>  
#include <exception>  
  
class TestClass  
{  
public:  
    ~TestClass()  
    {  
        printf("Destroying TestClass!\r\n");  
    }  
};  
  
__declspec(noinline) void TestCPPEX()  
{  
#ifdef CPPEX  
    printf("Throwing C++ exception\r\n");  
    throw std::exception("");  
#else  
    printf("Triggering SEH exception\r\n");  
    volatile int *pInt = 0x00000000;  
    *pInt = 20;  
#endif  
}  
  
__declspec(noinline) void TestExceptions()  
{  
    TestClass d;  
    TestCPPEX();  
}  
  
int main()  
{  
    __try  
    {  
        TestExceptions();  
    }  
    __except(EXCEPTION_EXECUTE_HANDLER)  
    {  
        printf("Executing SEH __except block\r\n");  
    }  
  
    return 0;  
}  
  
```  
  
 If you use **/EHsc** to compile this code but the local test control `CPPEX` is undefined, there is no execution of the `TestClass` destructor and the output looks like this:  
  
 **Triggering SEH exception**  
**Executing SEH __except block** If you use **/EHsc** to compile the code and `CPPEX` is defined by using `/DCPPEX` (so that a C++ exception is thrown), the `TestClass` destructor executes and the output looks like this:  
  
 **Throwing C++ exception**  
**Destroying TestClass!**  
**Executing SEH __except block** If you use **/EHa** to compile the code, the `TestClass` destructor executes regardless of whether the exception was thrown by using `std::throw` or by using SEH to trigger the exception (`CPPEX` defined or not). The output looks like this:  
  
 **Throwing C++ exception**  
**Destroying TestClass!**  
**Executing SEH __except block** For more information, see [/EH (Exception Handling Model)](../vs140/-EH--Exception-Handling-Model-.md).  
  
## END Microsoft Specific  
  
## See Also  
 [Exception Handling](../vs140/Exception-Handling-in-Visual-C--.md)   
 [Keywords](../vs140/Keywords--C---.md)   
 [<exception\> Header](../vs140/-exception-.md)   
 [Errors and Exception Handling (Modern C++)](../vs140/Errors-and-Exception-Handling--Modern-C---.md)   
 [Structured Exception Handling (Windows)](http://msdn.microsoft.com/library/windows/desktop/ms680657.aspx)