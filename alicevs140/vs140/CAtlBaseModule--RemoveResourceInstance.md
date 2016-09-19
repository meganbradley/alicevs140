---
title: "CAtlBaseModule::RemoveResourceInstance"
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
ms.assetid: 8be00109-28aa-42d4-9452-66164afc6a27
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlBaseModule::RemoveResourceInstance
Removes a resource instance from the list of stored handles.  
  
## Syntax  
  
```  
  
      bool RemoveResourceInstance(  
   HINSTANCE hInst   
) throw( );  
```  
  
#### Parameters  
 `hInst`  
 The resource instance to remove.  
  
## Return Value  
 Returns true if the resource was successfully removed, false otherwise.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CAtlBaseModule Class](../vs140/CAtlBaseModule-Class.md)   
 [CAtlBaseModule::AddResourceInstance](../vs140/CAtlBaseModule--AddResourceInstance.md)