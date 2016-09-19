---
title: "CLS Compliance Warning CLS01701"
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
ms.assetid: 6ccbe156-9017-44ea-bd4e-a838af2ec2e7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01701
Unmanaged pointer types are not CLS-compliant  
  
 A CLS-compliant constructor cannot contain a native pointer declaration.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS01701:  
  
```  
// CLS01701.cpp  
// compile with: /clr /LD  
// CLS01701 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
public ref class One {  
public:  
   One(int* Parameter) {}   // CLS01701  
};  
```