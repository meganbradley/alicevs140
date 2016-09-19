---
title: "CLS Compliance Warning CLS01206"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e72f2293-874b-406c-9f22-92aeb64ac732
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01206
The visibility and accessibility of types and members shall be such that types in the signature of any member shall be visible and accessible whenever the member itself is visible and accessible. For example, a public member function that is visible outside its assembly shall not have an argument whose type is visible only within the assembly.  
  
 Types in method signatures must have accessibility greater than or equal to that of the method.  For example, a public method that is visible outside its assembly shall not have an argument whose type is visible only within the assembly.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS01206:  
  
```  
/* CLS01206.cpp */  
// compile with: /clr /LD  
// CLS01206 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
public ref class PublicLevelType {};  
  
private ref class AssemblyLevelType {};  
  
public ref class One {  
public:  
   AssemblyLevelType^ Method1() {  
      return gcnew AssemblyLevelType();  
   }  
};  
```