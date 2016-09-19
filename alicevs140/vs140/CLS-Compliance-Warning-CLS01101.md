---
title: "CLS Compliance Warning CLS01101"
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
ms.assetid: 01034537-eee8-40e6-9139-d1788612738a
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01101
All types appearing in a signature shall be CLS-compliant  
  
 If a type is CLS compliant, then all constructors in the type, unless marked not CLS compliant, must have CLS compliant type parameters.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
## Example  
 The following sample generates CLS01101:  
  
```  
// CLS01101.cpp  
// compile with: /clr /LD  
// CLS01101 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
[CLSCompliant(true)]  
public ref class CompliantType {};  
  
[CLSCompliant(false)]  
public ref class NotCompliantType {};  
  
[CLSCompliant(true)]  
public ref class One {  
public:  
  
   One(NotCompliantType^ parameter) {}   // CLS01101  
  
   One(CompliantType^ parameter) {}   // OK  
  
   [CLSCompliant(false)]  
   One(NotCompliantType^ param1, NotCompliantType^ param2) {}   // OK  
};  
```