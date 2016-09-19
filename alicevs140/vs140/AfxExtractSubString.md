---
title: "AfxExtractSubString"
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
ms.topic: article
ms.assetid: eca6f230-7bb8-4cc3-80a1-265a6641a85c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxExtractSubString
This global function can be used to extract a substring from a given source string.  
  
## Syntax  
  
```  
  
      BOOL AFXAPI AfxExtractSubString (  
   CString& rString,  
   LPCTSTR lpszFullString,  
   int iSubString,  
   TCHAR chSep = '\n'  
);  
```  
  
#### Parameters  
 *rString*  
 -   Reference to a [CString](../vs140/Using-CString.md) object that will receive an individual substring.  
  
 *lpszFullString*  
 -   String containing the full text of the string to extract from.  
  
 *iSubString*  
 -   Zero-based index of the substring to extract from *lpszFullString*.  
  
 *chSep*  
 -   Separator character used to delimit substrings.  
  
## Return Value  
 **TRUE** if the function successfully extracted the substring at the provided index; otherwise, **FALSE**.  
  
## Remarks  
 This function is useful for extracting multiple substrings from a source string when a known single character separates each substring. This function searches from the beginning of the `lpszFullString` parameter each time it is called.  
  
 This function will return FALSE if either `lpszFullString` is set to **NULL** or the function reaches the end of `lpszFullString` without finding `iSubString`+1 occurrences of the specified separator character. The `rString` parameter will not be modified from its original value if `lpszFullString` was set to **NULL**; otherwise, the `rString` parameter is set to the empty string if the substring could not be extracted for the specified index.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#48](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#48)]  
  
## Requirements  
 **Header**: <afxwin.h>  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [Using CString](../vs140/Using-CString.md)