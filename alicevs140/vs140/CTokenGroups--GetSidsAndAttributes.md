---
title: "CTokenGroups::GetSidsAndAttributes"
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
ms.assetid: 2d060c76-b965-47e7-bbc7-866f1d9d2c16
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTokenGroups::GetSidsAndAttributes
Retrieves the `CSid` objects and (optionally) the attributes belonging to the `CTokenGroups` object.  
  
## Syntax  
  
```  
  
      void GetSidsAndAttributes(  
   CSid::CSidArray * pSids,  
   CAtlArray< DWORD > * pAttributes = NULL  
) const throw(...);  
```  
  
#### Parameters  
 `pSids`  
 Pointer to an array of [CSid](../vs140/CSid-Class.md) objects.  
  
 `pAttributes`  
 Pointer to an array of DWORDs. If this parameter is omitted or NULL, the attributes are not retrieved.  
  
## Remarks  
 This method will enumerate all of the `CSid` objects contained in the `CTokenGroups` object and place them and (optionally) the attribute flags into array objects.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CTokenGroups Class](../vs140/CTokenGroups-Class.md)   
 [CTokenGroups::LookupSid](../vs140/CTokenGroups--LookupSid.md)