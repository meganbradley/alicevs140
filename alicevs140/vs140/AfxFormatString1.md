---
title: "AfxFormatString1"
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
ms.assetid: 1dbba880-a467-46fa-a7f1-6e8778b1b480
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxFormatString1
Substitutes the string pointed to by `lpsz1` for any instances of the characters "%1" in the template string resource identified by `nIDS`.  
  
## Syntax  
  
```  
  
      void AfxFormatString1(  
   CString& rString,  
   UINT nIDS,  
   LPCTSTR lpsz1   
);   
```  
  
#### Parameters  
 `rString`  
 A reference to a `CString` object that will contain the resultant string after the substitution is performed.  
  
 `nIDS`  
 The resource ID of the template string on which the substitution will be performed.  
  
 `lpsz1`  
 A string that will replace the format characters "%1" in the template string.  
  
## Remarks  
 The newly formed string is stored in `rString`. For example, if the string in the string table is "File %1 not found", and `lpsz1` is equal to "C:\MYFILE.TXT", then `rString` will contain the string "File C:\MYFILE.TXT not found". This function is useful for formatting strings sent to message boxes and other windows.  
  
 If the format characters "%1" appear in the string more than once, multiple substitutions will be made.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#25)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxFormatString2](../vs140/AfxFormatString2.md)