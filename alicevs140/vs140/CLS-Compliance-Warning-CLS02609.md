---
title: "CLS Compliance Warning CLS02609"
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
ms.assetid: ea1afa9a-03d2-4417-af14-68e3b03a858f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS02609
A property and its accessors shall all be static, all be virtual, or all be instance  
  
 A property and its accessors shall not differ in their static, virtual, or instance qualifiers.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS02609:  
  
```  
// CLS02609.cpp  
// compile with: /clr /LD  
// CLS02609 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
public ref class One {  
private:  
   int InstanceMember;  
   static int StaticMember;  
public:  
  
   property int MyProperty1 {   // CLS02609  
   public:  
      void set(int value) {}  
      static int get() {  
         return StaticMember;  
      }  
   }  
  
   property int MyProperty2 {   // OK  
   public:  
      void set(int value) {}  
      int get() {  
         return StaticMember;  
      }  
   }  
};  
```