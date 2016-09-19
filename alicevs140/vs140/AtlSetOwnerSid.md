---
title: "AtlSetOwnerSid"
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
ms.assetid: 3a8abb76-1d2c-465d-a5e8-62a12a3c37f3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlSetOwnerSid
Call this function to set the owner security identifier (SID) of an object.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      inline bool AtlSetOwnerSid(  
HANDLE hObject,  
SE_OBJECT_TYPE ObjectType,  
const CSid& rSid  
) throw(...);  
```  
  
#### Parameters  
 `hObject`  
 Handle to the object for which to set security information.  
  
 `ObjectType`  
 Specifies a value from the [SE_OBJECT_TYPE](http://msdn.microsoft.com/library/windows/desktop/aa379593) enumeration that indicates the type of object identified by the `hObject` parameter.  
  
 `rSid`  
 The `CSid` object containing the new security information.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [Security Global Functions](../vs140/Security-Global-Functions.md)   
 [AtlGetOwnerSid](../vs140/AtlGetOwnerSid.md)   
 [CSid Class](../vs140/CSid-Class.md)