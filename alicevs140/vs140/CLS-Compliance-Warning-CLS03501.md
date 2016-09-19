---
title: "CLS Compliance Warning CLS03501"
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
ms.assetid: 26a08830-9c8a-4bf6-931d-e0c523f1eb21
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS03501
The CLS does not allow publicly visible required modifiers (modreq), but does allow optional modifiers (modopt) they do not understand  
  
 The CLS does not allow publicly visible required modifiers (modreq), but does allow optional modifiers (modopt) they do not understand.  
  
 Make sure that constructor signatures do not contain types marked with publicly visible required modifiers.  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS03501:  
  
```  
// CLS03501.cpp  
// compile with: /clr /LD  
// CLS03501 expected  
using namespace System;  
using namespace System::Reflection;  
using namespace cli::language;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
public ref class One {  
public:  
   One(volatile Int32 param) {}   // CLS03501  
   One( Int32 param1, Int32 param2) {}   // OK  
};  
```