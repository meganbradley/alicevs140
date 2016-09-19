---
title: "CLS Compliance Warning CLS01911"
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
ms.assetid: 673a701a-166b-4782-bff4-a198f70becd5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01911
CLS-compliant interfaces shall not define static methods, nor shall they define fields  
  
 A CLS-compliant interface cannot contain static methods or fields.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS01911:  
  
```  
// CLS01911.cpp  
// compile with: /clr /LD  
// CLS01911 expected  
  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
public interface class IOne {  
   static void Method1() {}   // interface static method not cls compliant  
};  
```