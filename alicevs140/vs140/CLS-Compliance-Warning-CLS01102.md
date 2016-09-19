---
title: "CLS Compliance Warning CLS01102"
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
ms.assetid: 49426c42-9d01-49ba-b061-ca0e8bd6782d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01102
All types appearing in a signature shall be CLS-compliant  
  
 If an event is CLS compliant, then all types used in the event access functions, unless marked not CLS compliant, must be CLS compliant types.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
```  
// CLS01102.cpp  
// compile with: /clr /LD  
// CLS01102 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
// Test types  
[CLSCompliant(true)]  
public delegate void CompliantType([parameter:CLSCompliant(true)] int parameter);  
  
[CLSCompliant(false)]  
public delegate void NotCompliantType([parameter:CLSCompliant(false)] int parameter);  
  
public ref class One {  
public:  
   event NotCompliantType^ MyEvent {  
   public:  
      void add(NotCompliantType^ Addparameter) {}  
      void remove(NotCompliantType^ Removeparameter) {}  
      void raise([parameter:CLSCompliant(false)] int parameter) {}  
   }  
};  
```