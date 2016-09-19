---
title: "CLS Compliance Warning CLS02409"
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
ms.assetid: 71d566ce-59c2-4d3d-97ff-72f4e9bd21ee
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS02409
The methods that implement the getter and setter methods of a property shall be marked SpecialName in the metadata  
  
 The methods that implement the getter and setter methods of a property were not marked with **specialname** in the metadata.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following function declaration (using MSIL assembly language) shows what could cause CLS02409:  
  
```  
.method public instance int32   
        get_MyProperty() cil managed  
```  
  
 By adding the **specialname** keyword, you can resolve this warning:  
  
```  
.method public specialname instance int32   
        get_MyProperty() cil managed  
```