---
title: "CAtlBaseModule::GetHInstanceAt"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 2a490c2f-91b1-4849-97bc-5d652316707c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlBaseModule::GetHInstanceAt
Returns a handle to a specified resource instance.  
  
## Syntax  
  
```  
  
      HINSTANCE GetHInstanceAt(  
   int i  
) throw( );  
```  
  
#### Parameters  
 *i*  
 The number of the resource instance.  
  
## Return Value  
 Returns the handle to the resource instance, or NULL if no corresponding resource instance exists.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CAtlBaseModule Class](../vs140/CAtlBaseModule-Class.md)   
 [CAtlBaseModule::AddResourceInstance](../vs140/CAtlBaseModule--AddResourceInstance.md)