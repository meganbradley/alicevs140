---
title: "Method &#39;&lt;methodname&gt;&#39; does not have a signature compatible with delegate &lt;&#39;delegatename&#39;&gt;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 88990637-7c92-467e-a3d3-db5498dc1dce
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Method &#39;&lt;methodname&gt;&#39; does not have a signature compatible with delegate &lt;&#39;delegatename&#39;&gt;
This error occurs when a conversion is required between a method and a delegate that is not possible. The cause of the error can be conversion between parameters or, when the method and delegate are functions, conversion in the return values.  
  
 The following code illustrates failed conversions. The delegate is `FunDel`.  
  
```vb#  
Delegate Function FunDel(ByVal i As Integer, ByVal d As Double) As Integer  
```  
  
 The following functions each differ from `FunDel` in a way that will cause this error.  
  
```vb#  
Function ExampleMethod1(ByVal m As Integer, ByVal aDate As Date) As Integer  
End Function  
  
Function ExampleMethod2(ByVal m As Integer, ByVal aDouble As Double) As Date  
End Function  
```  
  
 Each of the following assignment statements causes the error.  
  
```vb#  
Sub Main()  
    ' The second parameters of FunDel and ExampleMethod1, Double and Date,  
    ' are not compatible.  
    'Dim d1 As FunDel = AddressOf ExampleMethod1  
  
    ' The return types of FunDel and ExampleMethod2, Integer and Date,  
    ' are not compatible.  
    'Dim d2 As FunDel = AddressOf ExampleMethod2  
  
End Sub  
```  
  
 **Error ID:** BC31143  
  
### To correct this error  
  
-   Examine the corresponding parameters and, if they are present, return types to determine which pair is not compatible.  
  
## See Also  
 [Relaxed Delegate Conversion](../vs140/Relaxed-Delegate-Conversion--Visual-Basic-.md)   
 [NOT IN BUILD: Delegates and the AddressOf Operator](assetId:///7b2ed932-8598-4355-b2f7-5cedb23ee86f)