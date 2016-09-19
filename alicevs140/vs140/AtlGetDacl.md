---
title: "AtlGetDacl"
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
ms.assetid: a0973648-0d46-4c1a-914f-bda861fe5d19
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlGetDacl
Call this function to retrieve the discretionary access-control list (DACL) information of a specified object.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      inline bool AtlGetDacl(  
HANDLE hObject,  
SE_OBJECT_TYPE ObjectType,  
CDacl* pDacl  
) throw(   );  
```  
  
#### Parameters  
 `hObject`  
 Handle to the object for which to retrieve the security information.  
  
 `ObjectType`  
 Specifies a value from the [SE_OBJECT_TYPE](http://msdn.microsoft.com/library/windows/desktop/aa379593) enumeration that indicates the type of object identified by the `hObject` parameter.  
  
 `pDacl`  
 Pointer to a DACL object which will contain the retrieved security information.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 In debug builds, an assertion error will occur if either `hObject` or `pDacl` is invalid*.*  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [Security Global Functions](../vs140/Security-Global-Functions.md)   
 [AtlSetDacl](../vs140/AtlSetDacl.md)   
 [CDacl Class](../vs140/CDacl-Class.md)