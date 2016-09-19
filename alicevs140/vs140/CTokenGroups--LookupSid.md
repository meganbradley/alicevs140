---
title: "CTokenGroups::LookupSid"
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
ms.assetid: ff9e2352-985a-47b8-a8d9-becdbad0c347
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenGroups::LookupSid
Retrieves the attributes associated with a `CSid` object.  
  
## Syntax  
  
```  
  
      bool LookupSid(  
   const CSid & rSid,  
   DWORD * pdwAttributes = NULL  
) const throw( );  
```  
  
#### Parameters  
 `rSid`  
 The [CSid](../vs140/CSid-Class.md) object.  
  
 `pdwAttributes`  
 Pointer to a DWORD which will accept the `CSid` object's attribute. If omitted or NULL, the attribute will not be retrieved.  
  
## Return Value  
 Returns true if the `CSid` is found, false otherwise.  
  
## Remarks  
 Setting `pdwAttributes` to NULL provides a way of confirming the existence of the `CSid` without accessing the attribute. Note that this method should not be used to check access rights as incorrect results may occur under Windows 2000. Applications should instead use the [CAccessToken::CheckTokenMembership](../vs140/CAccessToken--CheckTokenMembership.md) method.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenGroups Class](../vs140/CTokenGroups-Class.md)   
 [CTokenGroups::GetSidsAndAttributes](../vs140/CTokenGroups--GetSidsAndAttributes.md)