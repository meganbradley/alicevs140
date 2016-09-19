---
title: "CAcl::GetAclEntry"
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
ms.assetid: 5cd2593b-88aa-4bbc-a606-e2add6e61f33
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAcl::GetAclEntry
Retrieves all of the information about an entry in an access-control list (ACL).  
  
## Syntax  
  
```  
  
      void GetAclEntry(   
   UINT nIndex,   
   CSid * pSid,   
   ACCESS_MASK * pMask = NULL,   
   BYTE * pType = NULL,   
   BYTE * pFlags = NULL,   
   GUID * pObjectType = NULL,   
   GUID * pInheritedObjectType = NULL   
) const throw(...);  
```  
  
#### Parameters  
 `nIndex`  
 Index to the ACL entry to retrieve.  
  
 `pSid`  
 The [CSid](../vs140/CSid-Class.md) object to which the ACL entry applies.  
  
 *pMask*  
 The mask specifying permissions to grant or deny access.  
  
 `pType`  
 The ACE type.  
  
 `pFlags`  
 The ACE flags.  
  
 `pObjectType`  
 The object type. This will be set to GUID_NULL if the object type is not specified in the ACE, or if the ACE is not an OBJECT ACE.  
  
 `pInheritedObjectType`  
 The inherited object type. This will be set to GUID_NULL if the inherited object type is not specified in the ACE, or if the ACE is not an OBJECT ACE.  
  
## Remarks  
 This method will retrieve all of the information about an individual ACE, providing more information than [CAcl::GetAclEntries](../vs140/CAcl--GetAclEntries.md) alone makes available.  
  
 See [ACE_HEADER](http://msdn.microsoft.com/library/windows/desktop/aa374919) for more details on ACE types and flags.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAcl Class](../vs140/CAcl-Class.md)   
 [CAcl::CAceFlagArray](../vs140/CAcl--CAceFlagArray.md)   
 [CAcl::CAceTypeArray](../vs140/CAcl--CAceTypeArray.md)   
 [ACCESS_MASK](http://msdn.microsoft.com/library/windows/desktop/aa374892)   
 [CAcl::GetAclEntries](../vs140/CAcl--GetAclEntries.md)