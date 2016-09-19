---
title: "CAcl::GetAclEntries"
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
ms.assetid: 8c8ebaaa-6bb9-47e5-adf2-f03078af0b50
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAcl::GetAclEntries
Retrieves the access-control list (ACL) entries from the `CAcl` object.  
  
## Syntax  
  
```  
  
      void GetAclEntries(  
   CSid::CSidArray * pSids,  
   CAccessMaskArray * pAccessMasks = NULL,  
   CAceTypeArray * pAceTypes = NULL,  
   CAceFlagArray * pAceFlags = NULL  
) const throw(...);  
```  
  
#### Parameters  
 `pSids`  
 A pointer to an array of [CSid](../vs140/CSid-Class.md) objects.  
  
 *pAccessMasks*  
 The access masks.  
  
 *pAceTypes*  
 The access-control entry (**ACE**) types.  
  
 *pAceFlags*  
 The **ACE** flags.  
  
## Remarks  
 This method fills the array parameters with the details of every **ACE** object contained in the `CAcl` object. Use NULL when the details for that particular array are not required.  
  
 The contents of each array correspond to each other, that is, the first element of the `CAccessMaskArray` array corresponds to the first element in the `CSidArray` array, and so on.  
  
 See [ACE_HEADER](http://msdn.microsoft.com/library/windows/desktop/aa374919) for more details on ACE types and flags.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAcl Class](../vs140/CAcl-Class.md)   
 [CAcl::CAceFlagArray](../vs140/CAcl--CAceFlagArray.md)   
 [CAcl::CAceTypeArray](../vs140/CAcl--CAceTypeArray.md)   
 [CAcl::CAccessMaskArray](../vs140/CAcl--CAccessMaskArray.md)   
 [CAcl::GetAclEntry](../vs140/CAcl--GetAclEntry.md)