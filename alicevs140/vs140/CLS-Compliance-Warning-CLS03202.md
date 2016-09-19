---
title: "CLS Compliance Warning CLS03202"
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
ms.assetid: 2219c86c-9276-4244-a2ff-bce578c4d65f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS03202
The add and remove methods for an event shall each take one parameter whose type defines the type of the event and that shall be derived from System.Delegate  
  
 The add and remove methods for an event shall each take one parameter whose type defines the type of the event and that shall be derived from System.Delegate.  
  
 For more information CLS compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following function declaration (using MSIL assembly language) shows what could cause CLS03202:  
  
```  
// bad  
.method public specialname instance void   
        add_MyEvent(class MyDelegate __unnamed000, int32 __extra) cil managed  
{}  
```  
  
 You can resolve this warning if the event accessor only takes one parameter:  
  
```  
.method public specialname instance void   
        add_MyEvent(class MyDelegate __unnamed000) cil managed   
{}  
```