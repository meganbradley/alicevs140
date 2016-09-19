---
title: "CTokenGroups::Delete"
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
ms.assetid: 37ca2022-9f47-4e6d-8524-feb2970b5ca4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenGroups::Delete
Deletes a `CSid` and its associated attributes from the `CTokenGroups` object.  
  
## Syntax  
  
```  
  
      bool Delete(  
   const CSid & rSid   
) throw( );  
```  
  
#### Parameters  
 `rSid`  
 The [CSid](../vs140/CSid-Class.md) object for which the security identifier (SID) and attributes should be removed.  
  
## Return Value  
 Returns true if the `CSid` is removed, false otherwise.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenGroups Class](../vs140/CTokenGroups-Class.md)   
 [CTokenGroups::DeleteAll](../vs140/CTokenGroups--DeleteAll.md)   
 [CTokenGroups::Add](../vs140/CTokenGroups--Add.md)