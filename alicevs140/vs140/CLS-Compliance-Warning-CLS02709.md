---
title: "CLS Compliance Warning CLS02709"
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
ms.assetid: 2dd2cf52-c602-43fa-818c-5ce90e507c79
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS02709
Type used in a property declaration was not CLS compliant  
  
 All types in a property declaration were not CLS-compliant.  
  
 For more information about properties, see [property](../vs140/property---C---Component-Extensions-.md).  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS02709:  
  
```  
// CLS02709.cpp  
// compile with: /clr /LD  
// CLS02709 expected  
using namespace System;  
using namespace System::Reflection;  
using namespace cli::language;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
public ref class One {  
   String^ LocalString;  
   int i;  
public:  
  
   // not CLS compliant  
   property interior_ptr<String^> MyProperty1 {  
  
      void set(interior_ptr<String^> value) {}  
  
      interior_ptr<String^> get() {  
         LocalString = "Hello";  
         return &LocalString;  
      }  
   }  
  
   // CLS compliant  
   property int MyProperty2 {  
  
      void set(int value) {}  
  
      int get() {  
         i = 1;  
         return i;  
      }  
   }  
};  
```