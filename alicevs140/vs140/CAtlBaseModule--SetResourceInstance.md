---
title: "CAtlBaseModule::SetResourceInstance"
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
ms.assetid: 116a2440-2e74-4f54-897a-d570ad88429e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlBaseModule::SetResourceInstance
Sets the resource instance of a `CAtlBaseModule` object.  
  
## Syntax  
  
```  
  
      HINSTANCE SetResourceInstance(  
   HINSTANCE hInst   
) throw( );  
```  
  
#### Parameters  
 `hInst`  
 The new resource instance.  
  
## Return Value  
 Returns the updated resource instance.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CAtlBaseModule Class](../vs140/CAtlBaseModule-Class.md)   
 [CAtlBaseModule::GetResourceInstance](../vs140/CAtlBaseModule--GetResourceInstance.md)