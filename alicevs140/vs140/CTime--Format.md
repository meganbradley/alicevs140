---
title: "CTime::Format"
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
ms.assetid: a1f2be7d-c1fd-4ec6-aa73-dd572da8ccf0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::Format
Call this member function to create a formatted representation of the date-time value.  
  
## Syntax  
  
```  
CString Format(  
   LPCTSTR pszFormat   
) const;  
CString Format(  
   UINT nFormatID   
) const;  
```  
  
#### Parameters  
 `pszFormat`  
 A formatting string similar to the `printf` formatting string. Formatting codes, preceded by a percent (`%`) sign, are replaced by the corresponding `CTime` component. Other characters in the formatting string are copied unchanged to the returned string. See the run-time function [strftime](../vs140/strftime--wcsftime--_strftime_l--_wcsftime_l.md) for a list of formatting codes.  
  
 `nFormatID`  
 The ID of the string that identifies this format.  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) that contains the formatted time.  
  
## Remarks  
 If the status of this `CTime` object is null, the return value is an empty string.  
  
 This method throws an exception if the date-time value to format does not range from midnight, January 1, 1970 through December 31, 3000 Universal Coordinated Time (UTC).  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#149](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#149)]  
  
## Requirements  
 Header: atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTime::FormatGmt](../vs140/CTime--FormatGmt.md)