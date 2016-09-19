---
title: "CTime::FormatGmt"
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
ms.assetid: 4853b29f-fee6-4b61-a8d5-6994bf86ab61
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTime::FormatGmt
Generates a formatted string that corresponds to this `CTime` object.  
  
## Syntax  
  
```  
CString FormatGmt(  
   LPCTSTR pszFormat   
) const;  
CString FormatGmt(  
   UINT nFormatID   
) const;  
```  
  
#### Parameters  
 `pszFormat`  
 Specifies a formatting string similar to the `printf` formatting string. See the run-time function [strftime](../vs140/strftime--wcsftime--_strftime_l--_wcsftime_l.md) for details.  
  
 `nFormatID`  
 The ID of the string that identifies this format.  
  
## Return Value  
 A [CString](../vs140/CStringT-Class.md) that contains the formatted time.  
  
## Remarks  
 The time value is not converted and thus reflects UTC.  
  
 This method throws an exception if the date-time value to format does not range from midnight, January 1, 1970 through December 31, 3000 Universal Coordinated Time (UTC).  
  
## Example  
 See the example for [CTime::Format](../vs140/CTime--Format.md).  
  
## Requirements  
 Header: atltime.h  
  
## See Also  
 [CTime Class](../Topic/CTime%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTime::Format](../vs140/CTime--Format.md)