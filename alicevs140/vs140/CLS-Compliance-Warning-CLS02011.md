---
title: "CLS Compliance Warning CLS02011"
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
ms.assetid: 9466be1e-9558-49e8-9ea4-5cfc54a22066
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS02011
CLS-compliant classes, value types, and interfaces shall not require the implementation of non-CLS-compliant interfaces  
  
 A typed marked as CLS compliant has one or more base types that are not CLS compliant.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS02011:  
  
```  
// CLS02011.cpp  
// compile with: /clr /LD  
// CLS02011 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
[CLSCompliant(true)]  
public interface class CompliantInterface {};  
  
[CLSCompliant(false)]  
public interface class NotCompliantInterface {};  
  
public ref class One : public NotCompliantInterface {};   // CLS02011   
public ref class Two : public CompliantInterface {};   // OK  
```