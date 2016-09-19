---
title: "How to: Retrieve the Current Username (C++-CLI)"
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
ms.topic: article
H1: How to: Retrieve the Current Username (C++/CLI)
ms.assetid: 91679571-d029-41f5-b657-1460c81c608a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Retrieve the Current Username (C++-CLI)
The following code example demonstrates the retrieval of the current user name (the name of the user logged into Windows). The name is stored in the <xref:System.Environment.UserName?qualifyHint=False> string, which is defined in the <xref:System.Environment?qualifyHint=False> namespace.  
  
## Example  
  
```  
// username.cpp  
// compile with: /clr  
using namespace System;  
  
int main()   
{  
   Console::WriteLine("\nCurrent user: {0}", Environment::UserName);  
   return 0;  
}  
```  
  
## See Also  
 [Windows Operations in C++](../Topic/Windows%20Operations%20\(C++-CLI\).md)   
 [.NET Programming in C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)