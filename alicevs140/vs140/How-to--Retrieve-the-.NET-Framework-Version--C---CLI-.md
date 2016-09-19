---
title: "How to: Retrieve the .NET Framework Version (C++-CLI)"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
H1: How to: Retrieve the .NET Framework Version (C++/CLI)
ms.assetid: fc786fbc-c915-4b15-bcad-0d68cf2c44bd
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Retrieve the .NET Framework Version (C++-CLI)
The following code example demonstrates how to determine the version of the currently installed .NET Framework with the <xref:System.Environment.Version?qualifyHint=False> property, which is a pointer to a <xref:System.Version?qualifyHint=False> object that contains the version information.  
  
## Example  
  
```  
// dotnet_ver.cpp  
// compile with: /clr  
using namespace System;  
int main()   
{  
   Version^ version = Environment::Version;  
   if (version)  
   {  
      int build = version->Build;  
      int major = version->Major;  
      int minor = version->Minor;  
      int revision = Environment::Version->Revision;  
      Console::Write(".NET Framework version: ");  
      Console::WriteLine("{0}.{1}.{2}.{3}",   
            build, major, minor, revision);  
   }  
   return 0;  
}  
```  
  
## See Also  
 [Windows Operations in C++](../Topic/Windows%20Operations%20\(C++-CLI\).md)   
 [.NET Programming in C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)