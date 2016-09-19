---
title: "CTimeSpan::Format"
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
ms.assetid: 1d21f250-8aef-41da-9454-cff08740db8b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTimeSpan::Format
Generates a formatted string that corresponds to this `CTimeSpan`.  
  
## Syntax  
  
```  
  
      CString Format(  
   LPCSTR pFormat   
) const;  
CString Format(  
   LPCTSTR pszFormat   
) const;  
CString Format(  
   UINT nID   
) const;  
```  
  
#### Parameters  
 `pFormat`, `pszFormat`  
 A formatting string similar to the `printf` formatting string. Formatting codes, preceded by a percent (`%`) sign, are replaced by the corresponding `CTimeSpan` component. Other characters in the formatting string are copied unchanged to the returned string. The value and meaning of the formatting codes for **Format** are listed below:  
  
-   **%D** Total days in this `CTimeSpan`  
  
-   **%H** Hours in the current day  
  
-   **%M** Minutes in the current hour  
  
-   **%S** Seconds in the current minute  
  
-   **%%** Percent sign  
  
 `nID`  
 The ID of the string that identifies this format.  
  
## Return Value  
 A `CString` object that contains the formatted time.  
  
## Remarks  
 The Debug version of the library checks the formatting codes and asserts if the code is not in the list above.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#163](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#163)]  
  
## Requirements  
 **Header:** atltime.h  
  
## See Also  
 [CTimeSpan Class](../vs140/CTimeSpan-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)