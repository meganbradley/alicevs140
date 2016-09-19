---
title: "CLS Compliance Warning CLS03514"
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
ms.assetid: b2d326ce-8c1b-4351-80d1-ccd1818b1ea3
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS03514
The CLS does not allow publicly visible required modifiers (modreq), but does allow optional modifiers (modopt) they do not understand  
  
 The CLS does not allow publicly visible required modifiers (modreq), but does allow optional modifiers (modopt) they do not understand.  
  
 Make sure that delegate signatures do not contain types marked with publicly visible required modifiers.  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS03514:  
  
```  
// CLS03514.cpp  
// compile with: /clr /LD  
// CLS03514 expected  
using namespace System;  
using namespace System::Reflection;  
using namespace cli::language;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
public delegate void MyDel(volatile Int32 param);   // CLS03514  
public delegate void MyDel2(Int32 param);   // OK  
```