---
title: "CLS Compliance Warning CLS01202"
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
ms.assetid: ab75e9c4-9d87-4bb4-ad8f-3e6ab5559de7
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01202
The visibility and accessibility of types and members shall be such that types in the signature of any member shall be visible and accessible whenever the member itself is visible and accessible. For example, a public event that is visible outside its assembly shall not have an argument whose type is visible only within the assembly.  
  
 The type of an event handler must have an accessibility that is greater than or equal to the accessibility of the event handler.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS01202:  
  
```  
/* CLS01202.cpp */  
// compile with: /clr /LD  
// CLS01202 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
public delegate void MyPublicDelegate();  
private delegate void MyAssemblyDelegate();  
  
public ref class One {  
public:  
   event MyAssemblyDelegate^ MyEvent {  
   public:  
      void add(MyAssemblyDelegate^ Addparameter) {}   //  not cls compliant  
      void remove(MyAssemblyDelegate^ Removeparameter) {}   //  not cls compliant  
      void raise() {}  
   }  
};  
```