---
title: "CTokenGroups::Add"
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
ms.assetid: 095d9e29-98aa-4fb7-83c7-ff7ca1085606
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenGroups::Add
Adds a `CSid` or existing **TOKEN_GROUPS** structure to the `CTokenGroups` object.  
  
## Syntax  
  
```  
  
      void Add(  
   const CSid & rSid,  
   DWORD dwAttributes   
) throw(...);  
void Add(  
   const TOKEN_GROUPS & rTokenGroups   
) throw(...);  
```  
  
#### Parameters  
 `rSid`  
 A [CSid](../vs140/CSid-Class.md) object.  
  
 `dwAttributes`  
 The attributes to associate with the `CSid` object.  
  
 *rTokenGroups*  
 A [TOKEN_GROUPS](http://msdn.microsoft.com/library/windows/desktop/aa379624) structure.  
  
## Remarks  
 These methods add one or more `CSid` objects and their associated attributes to the `CTokenGroups` object.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenGroups Class](../vs140/CTokenGroups-Class.md)