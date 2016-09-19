---
title: "CLS Compliance Warning CLS02311"
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
ms.assetid: 2faddffb-866d-417f-9ff3-9c61616030fb
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS02311
A CLS-compliant class shall inherit from a CLS-compliant class  
  
 A CLS-compliant class shall inherit from a CLS-compliant class.  For example, 'System::Object'.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS02311:  
  
```  
// CLS02311.cpp  
// compile with: /clr /LD  
// CLS02311 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:CLSCompliant (true)];  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
  
[CLSCompliant(true)]  
public ref class CompliantType {};  
  
[CLSCompliant(false)]  
public ref class NotCompliantType {};  
  
public ref class One : public NotCompliantType {};   // CLS02311   
public ref class Two : public CompliantType {};   // OK  
```