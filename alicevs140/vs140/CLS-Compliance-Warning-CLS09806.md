---
title: "CLS Compliance Warning CLS09806"
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
ms.assetid: fc97cf0e-c72e-4c09-96be-f90f9840e76e
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS09806
Generic methods are not CLS-compliant  
  
 A generic method is not CLS compliant.  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS09806:  
  
```  
// CLS09806.cpp  
// compile with: /clr /LD /link /noentry  
// CLS09806 expected  
using namespace System::Reflection;  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
using namespace System;  
[assembly:CLSCompliant (true)];  
  
generic <class T> public ref struct One {  
public:  
   generic <class U> void Method1() {}  
};  
```