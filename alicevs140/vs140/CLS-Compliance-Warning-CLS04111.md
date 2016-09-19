---
title: "CLS Compliance Warning CLS04111"
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
ms.assetid: 4b445ce7-d823-4cf3-b971-1c181be5fa41
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS04111
Attributes shall be of type 'System::Attribute', or inherit from it  
  
 In order to be CLS compliant, a custom attribute must inherit from System::Attribute.  An attribute that did not inherit from System::Attribute was applied to a type.  
  
 The following declaration (using MSIL assembly language) shows what could cause CLS04111:  
  
```  
.class public auto ansi MyAttribute  
       extends [mscorlib]System.Object  
```  
  
 Causing the attribute to derive from System::Attribute resolves the warning:  
  
```  
.class public auto ansi MyAttribute  
       extends [mscorlib]System.Attribute  
```