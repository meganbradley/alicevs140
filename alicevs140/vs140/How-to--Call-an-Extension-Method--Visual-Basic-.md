---
title: "How to: Call an Extension Method (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: df07750f-40f4-4c07-a79e-1113a27cfbea
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Call an Extension Method (Visual Basic)
Extension methods enable you to add methods to an existing class. After an extension method is declared and brought into scope, you can call it like an instance method of the type that it extends. For more information about how to write an extension method, see [How to: Write an Extension Method](../vs140/How-to--Write-an-Extension-Method--Visual-Basic-.md).  
  
 The following instructions refer to extension method `PrintAndPunctuate`, which will display the string instance that invokes it, followed by whatever value is sent in for the second parameter, `punc`.  
  
```vb#  
Imports System.Runtime.CompilerServices  
  
Module StringExtensions  
    <Extension()>   
    Public Sub PrintAndPunctuate(ByVal aString As String,   
                                 ByVal punc As String)  
        Console.WriteLine(aString & punc)  
    End Sub  
  
End Module  
  
```  
  
 The method must be in scope when it is called.  
  
### To call an extension method  
  
1.  Declare a variable that has the data type of the first parameter of the extension method. For `PrintAndPunctuate`, you need a <xref:System.String?qualifyHint=False> variable:  
  
    ```  
    Dim example = "Ready"  
    ```  
  
2.  That variable will invoke the extension method, and its value is bound to the first parameter, `aString`. The following calling statement will display `Ready?`.  
  
    ```  
    example.PrintAndPunctuate("?")  
    ```  
  
     Notice that the call to this extension method looks just like a call to any one of the <xref:System.String?qualifyHint=False> instance methods that require one parameter:  
  
    ```  
    example.EndsWith("dy")  
    example.IndexOf("R")  
    ```  
  
3.  Declare another string variable and call the method again to see that it works with any string.  
  
    ```  
    Dim example2 = " or not"  
    example2.PrintAndPunctuate("!!!")  
    ```  
  
     The result this time is: `or not!!!`.  
  
## Example  
 The following code is a complete example of the creation and use of a simple extension method.  
  
```vb#  
Imports System.Runtime.CompilerServices  
Imports ConsoleApplication1.StringExtensions  
  
Module Module1  
  
    Sub Main()  
  
        Dim example = "Hello"  
        example.PrintAndPunctuate(".")  
        example.PrintAndPunctuate("!!!!")  
  
        Dim example2 = "Goodbye"  
        example2.PrintAndPunctuate("?")  
    End Sub  
  
    <Extension()>   
    Public Sub PrintAndPunctuate(ByVal aString As String,   
                                 ByVal punc As String)  
        Console.WriteLine(aString & punc)  
    End Sub  
End Module  
  
' Output:  
' Hello.  
' Hello!!!!  
' Goodbye?  
```  
  
## See Also  
 [How to: Write an Extension Method](../vs140/How-to--Write-an-Extension-Method--Visual-Basic-.md)   
 [Extension Methods](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Scope in Visual Basic](../vs140/Scope-in-Visual-Basic.md)