---
title: "CLS Compliance Warning CLS01512"
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
ms.assetid: 15822eb3-43b1-4d58-a22d-9532e5820008
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01512
The varargs constraint is not part of the CLS  
  
 The varargs constraint is not part of the Common Language Subset (CLS).  The only calling convention supported by the CLS is the standard managed calling convention.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following function declaration (using MSIL assembly language) shows what could cause CLS01512:  
  
```  
.method public specialname rtspecialname static   
        vararg void  .cctor() cil managed  
```  
  
 By removing the **vararg** keyword, you can resolve this warning:  
  
```  
.method public specialname rtspecialname static   
        void  .cctor() cil managed  
```