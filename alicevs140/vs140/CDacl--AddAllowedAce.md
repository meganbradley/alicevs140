---
title: "CDacl::AddAllowedAce"
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
ms.assetid: 2c377c42-df8b-4a95-920c-edf6676ec5f2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDacl::AddAllowedAce
Adds an allowed ACE (access-control entry) to the `CDacl` object.  
  
## Syntax  
  
```  
  
      bool AddAllowedAce(  
   const CSid & rSid,  
   ACCESS_MASK AccessMask,  
   BYTE AceFlags = 0  
) throw(...);  
bool AddAllowedAce(  
   const CSid & rSid,  
   ACCESS_MASK AccessMask,  
   BYTE AceFlags,  
   const GUID * pObjectType,  
   const GUID * pInheritedObjectType  
) throw(...);  
```  
  
#### Parameters  
 `rSid`  
 A [CSid](../vs140/CSid-Class.md) object.  
  
 `AccessMask`  
 Specifies the mask of access rights to be allowed for the specified `CSid` object.  
  
 `AceFlags`  
 A set of bit flags that control ACE inheritance.  
  
 `pObjectType`  
 The object type.  
  
 `pInheritedObjectType`  
 The inherited object type.  
  
## Return Value  
 Returns **true** if the ACE is added to the `CDacl` object, **false** on failure.  
  
## Remarks  
 A `CDacl` object contains zero or more ACEs (access-control entries) that identify the users and groups who can access the object. This method adds an ACE that allows access to the `CDacl` object.  
  
> [!NOTE]
>  The second form of `AddAllowedAce` is only available on Windows 2000 and later.  
  
 See [ACE_HEADER](http://msdn.microsoft.com/library/windows/desktop/aa374919) for a description of the various flags which can be set in the `AceFlags` parameter.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CDacl Class](../vs140/CDacl-Class.md)   
 [CDacl::AddDeniedAce](../vs140/CDacl--AddDeniedAce.md)   
 [ACCESS_MASK](http://msdn.microsoft.com/library/windows/desktop/aa374892)