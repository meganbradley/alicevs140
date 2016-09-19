---
title: "CLS Compliance Warning CLS09911"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8cc0b0c0-a823-4392-9bf9-4d12242ef451
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS09911
Generic types are not CLS-compliant  
  
 A CLS-compliant type cannot also be a generic type.  For more information about generics in Visual C++, see [Support for Generics in C++](../vs140/Generics---C---Component-Extensions-.md).  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS09911:  
  
```  
// CLS09911.cpp  
// compile with: /clr /LD  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
generic <class T>  
public ref class Five {   // CLS09911  
};  
  
```