---
title: "CLS Compliance Warning CLS04101"
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
ms.assetid: 5ad21eb4-0c6e-4629-bc4a-af274f8a8d90
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS04101
Attributes shall be of type 'System::Attribute', or inherit from it  
  
 Make sure that all attributes applied to constructor parameters have type 'System.Attribute' or inherit from it.  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following declaration (using MSIL assembly language) shows what could cause CLS04101:  
  
```  
.class public auto ansi MyAttribute extends [mscorlib]System.Object  
{  
  .method public specialname rtspecialname instance void  .ctor() cil managed  
```  
  
 Causing the attribute to derive from System::Attribute resolves the warning:  
  
```  
.class public auto ansi MyAttribute extends [mscorlib]System.Object  
{  
  .method public specialname rtspecialname instance void  .ctor() cil managed  
```