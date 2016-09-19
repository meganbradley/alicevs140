---
title: "Dynamic Object Creation"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3e0f51cb-3e24-4231-817f-1c0ce9f2d5df
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Dynamic Object Creation
This article explains how to create an object dynamically at run time. The procedure uses run-time class information, as discussed in the article [Accessing Run-Time Class Information](../vs140/Accessing-Run-Time-Class-Information.md).  
  
#### To dynamically create an object given its run-time class  
  
1.  Use the following code to dynamically create an object by using the `CreateObject` function of the `CRuntimeClass`. Note that on failure, `CreateObject` returns **NULL** instead of raising an exception:  
  
     [!CODE [NVC_MFCCObjectSample#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#6)]  
  
## See Also  
 [Using CObject](../vs140/Using-CObject.md)