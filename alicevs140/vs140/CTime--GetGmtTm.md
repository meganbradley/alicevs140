---
title: "CTime::GetGmtTm"
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
ms.assetid: 2aed9533-496b-4f2c-9a72-b21af9eb5360
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::GetGmtTm
Gets a **struct tm** that contains a decomposition of the time contained in this `CTime` object.  
  
## Syntax  
  
```  
  
      struct tm* GetGmtTm(  
   struct tm* ptm   
) const;  
```  
  
#### Parameters  
 `ptm`  
 Points to a buffer that will receive the time data. If this pointer is **NULL**, an exception is thrown.  
  
## Return Value  
 A pointer to a filled-in **struct tm** as defined in the include file TIME.H. See [gmtime, _gmtime32, _gmtime64](../vs140/gmtime--_gmtime32--_gmtime64.md) for the structure layout.  
  
## Remarks  
 `GetGmtTm` returns UTC.  
  
 `ptm` cannot be `NULL`. If you want to revert to the old behavior, in which `ptm` could be `NULL` to indicate that an internal, statically allocated buffer should be used, then undefine `_SECURE_ATL`.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#155](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#155)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)