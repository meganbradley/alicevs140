---
title: "AtlGetOwnerSid"
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
ms.assetid: 0e3a2606-74b8-4412-9803-bb437e22da85
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlGetOwnerSid
Call this function to retrieve the owner security identifier (SID) of an object.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      inline bool AtlGetOwnerSid(  
HANDLE hObject,  
SE_OBJECT_TYPE ObjectType,  
CSid* pSid   
) throw(...);  
```  
  
#### Parameters  
 `hObject`  
 Handle to the object from which to retrieve security information.  
  
 `ObjectType`  
 Specifies a value from the [SE_OBJECT_TYPE](http://msdn.microsoft.com/library/windows/desktop/aa379593) enumeration that indicates the type of object identified by the `hObject` parameter.  
  
 `pSid`  
 Pointer to a `CSid` object which will contain the new security information.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [Security Global Functions](../vs140/Security-Global-Functions.md)   
 [AtlSetOwnerSid](../vs140/AtlSetOwnerSid.md)   
 [CSid Class](../vs140/CSid-Class.md)