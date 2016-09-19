---
title: "CLS Compliance Warning CLS00500"
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
ms.assetid: faaf377e-3738-4c0d-9a51-09db4073564e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS00500
All names in a CLS-compliant scope shall be distinct independent of kind  
  
 All names introduced in a CLS-compliant scope shall be distinct independent of kind, except where the names are identical and resolved via overloading. For CLS purposes, two names are the same if their lowercase mappings are the same. Only properties and functions may be overloaded. When overloaded, properties and functions shall be overloaded based only on the number and types of their parameters, except the conversion operators, which may also be overloaded based on their return type; see [User-Defined Conversions](../vs140/User-Defined-Conversions--C---CLI-.md) for more information.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS00500:  
  
```  
// CLS00500.cpp  
// compile with: /clr /LD  
// CLS00500 expected  
using namespace System;  
using namespace System::Reflection;  
[assembly:AssemblyKeyFile("clscompliance.snk")];  
[assembly:System::CLSCompliant(true)];  
  
public ref class a {};  
public ref class A {};   // CLS00500  
```