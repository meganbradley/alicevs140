---
title: "CTokenPrivileges::GetLuidsAndAttributes"
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
ms.assetid: 84b32749-f7ed-4fd6-8c3d-3073095477af
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenPrivileges::GetLuidsAndAttributes
Retrieves the locally unique identifiers (LUIDs) and attribute flags from the `CTokenPrivileges` object.  
  
## Syntax  
  
```  
  
      void GetLuidsAndAttributes(  
   CLUIDArray * pPrivileges,  
   CAttributes * pAttributes = NULL   
) const throw(...);  
```  
  
#### Parameters  
 `pPrivileges`  
 Pointer to an array of [LUID](http://msdn.microsoft.com/library/windows/desktop/aa379261) objects. **CLUIDArray** is a typedef defined as **CAtlArray<LUID\> CLUIDArray**.  
  
 `pAttributes`  
 Pointer to an array of DWORD objects. If this parameter is omitted or NULL, the attributes are not retrieved. **CAttributes** is a typedef defined as **CAtlArray <DWORD\> CAttributes**.  
  
## Remarks  
 This method will enumerate all of the privileges contained in the `CTokenPrivileges` access token object and place the individual LUIDs and (optionally) the attribute flags into array objects.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenPrivileges Class](../vs140/CTokenPrivileges-Class.md)   
 [CTokenPrivileges::GetNamesAndAttributes](../vs140/CTokenPrivileges--GetNamesAndAttributes.md)   
 [CTokenPrivileges::LookupPrivilege](../vs140/CTokenPrivileges--LookupPrivilege.md)   
 [CTokenPrivileges::GetDisplayNames](../vs140/CTokenPrivileges--GetDisplayNames.md)   
 [LUID_AND_ATTRIBUTES](http://msdn.microsoft.com/library/windows/desktop/aa379263)