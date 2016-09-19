---
title: "CLS Compliance Warning CLS01203"
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
ms.assetid: fe27463a-27df-473b-985a-b04c3bfac4d3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01203
The visibility and accessibility of types and members shall be such that types in the signature of any member shall be visible and accessible whenever the member itself is visible and accessible. For example, a public field that is visible outside its assembly shall not be of a type that is visible only within the assembly.  
  
 The visibility and accessibility of types and members shall be such that types in the signature of any member shall be visible and accessible whenever the member itself is visible and accessible. For example, a public field that is visible outside its assembly shall not be of a type that is visible only within the assembly.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS01203:  
  
```  
/* CLS01203.cpp */  
// compile with: /clr /LD  
// CLS01203 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
public ref class PublicLevelType {};  
private ref class AssemblyLevelType {};  
  
public ref class One {  
public:  
   AssemblyLevelType^ Member1;   // not cls compliant  
   PublicLevelType^ Member2;   // cls compliant  
};  
```