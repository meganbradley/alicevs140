---
title: "How to: Determine the User Interactive State (C++-CLI)"
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
H1: How to: Determine the User Interactive State (C++/CLI)
ms.assetid: 9f52323e-38b8-4a41-9b1d-052012ad839b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Determine the User Interactive State (C++-CLI)
The following code example demonstrates how to determine whether code is being run in a user-interactive context. If <xref:System.Environment.UserInteractive?qualifyHint=False> is false, then the code is running as a service process or from inside a Web application, in which case you should not attempt to interact with the user.  
  
## Example  
  
```  
// user_interactive.cpp  
// compile with: /clr  
using namespace System;  
  
int main()   
{  
   if ( Environment::UserInteractive )  
      Console::WriteLine("User interactive");  
   else  
      Console::WriteLine("Noninteractive");  
   return 0;  
}  
```  
  
## See Also  
 [Windows Operations in C++](../Topic/Windows%20Operations%20\(C++-CLI\).md)   
 [.NET Programming in C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)