---
title: "CAtlBaseModule::AddResourceInstance"
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
ms.assetid: 94a35dfb-c908-4f20-b3bf-ceffab8c1e46
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlBaseModule::AddResourceInstance
Adds a resource instance to the list of stored handles.  
  
## Syntax  
  
```  
  
      bool AddResourceInstance(  
   HINSTANCE hInst   
) throw( );  
```  
  
#### Parameters  
 `hInst`  
 The resource instance to add.  
  
## Return Value  
 Returns true if the resource was successfully added, false otherwise.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CAtlBaseModule Class](../vs140/CAtlBaseModule-Class.md)   
 [CAtlBaseModule::GetHInstanceAt](../vs140/CAtlBaseModule--GetHInstanceAt.md)   
 [CAtlBaseModule::RemoveResourceInstance](../vs140/CAtlBaseModule--RemoveResourceInstance.md)