---
title: "CLS Compliance Warning CLS01703"
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
ms.assetid: b03ae369-3c4b-4080-9b78-4c9bfba581a3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01703
Unmanaged pointer types are not CLS-compliant  
  
 A CLS-compliant field cannot contain a native pointer declaration.  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS01703:  
  
```  
// CLS01703.cpp  
// compile with: /clr /LD  
// CLS01703 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
public ref class MyClass {  
public:  
   int* Parameter;   // CLS01703  
};  
```