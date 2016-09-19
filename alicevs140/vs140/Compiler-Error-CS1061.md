---
title: "Compiler Error CS1061"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 10ba0509-d541-43da-acf5-eaa7987e41d4
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1061
'type' does not contain a definition for 'member' and no extension method 'name' accepting a first argument of type 'type' could be found (are you missing a using directive or an assembly reference?).  
  
 This error occurs when you try to call a method or access a class member that does not exist.  
  
## Example  
 The following example generates CS1061 because `TestClass1` does not have a `DisplaySomething` method. It does have a method that is called `WriteSomething`. Perhaps that is what the author of this source code meant to write.  
  
```c#  
// cs1061.cs  
public class TestClass1  
{  
    // TestClass1 has one method, called WriteSomething.  
    public void WriteSomething(string s)  
    {  
        System.Console.WriteLine(s);  
    }  
}  
  
public class TestClass2  
{  
    // TestClass2 has one method, called DisplaySomething.  
    public void DisplaySomething(string s)  
    {  
        System.Console.WriteLine(s);  
    }  
}  
  
public class TestTheClasses  
{  
    public static void Main()  
    {  
        TestClass1 tc1 = new TestClass1();  
        TestClass2 tc2 = new TestClass2();  
        // The following call fails because TestClass1 does not have   
        // a method called DisplaySomething.  
        tc1.DisplaySomething("Hello");      // CS1061  
  
        // To correct the error, change the method call to either   
        // tc1.WriteSomething or tc2.DisplaySomething.  
        tc1.WriteSomething("Hello from TestClass1");  
        tc2.DisplaySomething("Hello from TestClass2");  
    }  
}  
```  
  
## See Also  
 [Classes and Structs (C# Programming Guide)](../Topic/Classes%20and%20Structs%20\(C%23%20Programming%20Guide\).md)   
 [Extension Methods (C# Programming Guide)](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)