---
title: "AfxFormatString2"
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
ms.assetid: 91b0c49b-be54-433a-9151-303e807e9607
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AfxFormatString2
Substitutes the string pointed to by `lpsz1` for any instances of the characters "%1", and the string pointed to by `lpsz2` for any instances of the characters "%2", in the template string resource identified by `nIDS`.  
  
## Syntax  
  
```  
  
      void AfxFormatString2(  
   CString& rString,  
   UINT nIDS,  
   LPCTSTR lpsz1,  
   LPCTSTR lpsz2   
);   
```  
  
#### Parameters  
 `rString`  
 A reference to the `CString` that will contain the resultant string after the substitution is performed.  
  
 `nIDS`  
 The string table ID of the template string on which the substitution will be performed.  
  
 `lpsz1`  
 A string that will replace the format characters "%1" in the template string.  
  
 `lpsz2`  
 A string that will replace the format characters "%2" in the template string.  
  
## Remarks  
 The newly formed string is stored in `rString`. For example, if the string in the string table is "File %1 not found in directory %2", `lpsz1` points to "MYFILE.TXT", and `lpsz2` points to "C:\MYDIR", then `rString` will contain the string "File MYFILE.TXT not found in directory C:\MYDIR"  
  
 If the format characters "%1" or "%2" appear in the string more than once, multiple substitutions will be made. They do not have to be in numerical order.  
  
## Example  
 [!CODE [NVC_MFC_Utilities#26](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_Utilities#26)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [AfxFormatString1](../vs140/AfxFormatString1.md)