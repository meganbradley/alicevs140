---
title: "CLS Compliance Warning CLS04113"
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
ms.assetid: 628f56bf-5f2f-4245-b4fd-02d4605a901c
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS04113
**Attributes shall be of type 'System::Attribute', or inherit from it**  
  
 In order to be CLS compliant, a custom attribute must inherit from System::Attribute.  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following declaration (using MSIL assembly language) shows what could cause CLS04100:  
  
```  
.class public auto ansi MyAttribute  
       extends [mscorlib]System.Object  
```  
  
 Causing the attribute to derive from System::Attribute resolves the warning:  
  
```  
.class public auto ansi MyAttribute  
       extends [mscorlib]System.Attribute  
```