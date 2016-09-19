---
title: "Compiler Error CS1026"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 782c0570-19c2-425d-aa41-565d33aa9bc0
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1026
) expected  
  
 An incomplete statement was found.  
  
 A common cause of this error is placing a statement, rather than an expression, within an inline expression in an ASP.NET page. For example, the following is incorrect:  
  
```  
<%=new TimeSpan(DateTime.Now.Ticks - new DateTime(2001, 1, 1).Ticks).Days;%>  
```  
  
 The following is correct:  
  
```  
<%=new TimeSpan(DateTime.Now.Ticks - new DateTime(2001, 1, 1).Ticks).Days %>  
```  
  
 It is interpreted as follows:  
  
```  
<% Response.Write(new TimeSpan(DateTime.Now.Ticks - new DateTime(2001, 1, 1).Ticks).Days); %>  
```  
  
 The following example generates CS1026:  
  
```  
// CS1026.cs  
#if (a == b   // CS1026, add closing )  
#endif  
  
class x  
{  
   public static void Main()  
   {  
   }  
}  
```