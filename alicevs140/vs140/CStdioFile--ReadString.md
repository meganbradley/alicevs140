---
title: "CStdioFile::ReadString"
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
ms.assetid: 3380de82-8c28-4e8a-b24b-d5d9a94d4b2d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStdioFile::ReadString
Reads text data into a buffer, up to a limit of `nMax`–1 characters, from the file associated with the `CStdioFile` object.  
  
## Syntax  
  
```  
  
      virtual LPTSTR ReadString(  
   LPTSTR lpsz,  
   UINT nMax   
);  
virtual BOOL ReadString(  
   CString& rString  
);  
```  
  
#### Parameters  
 `lpsz`  
 Specifies a pointer to a user-supplied buffer that will receive a null-terminated text string.  
  
 `nMax`  
 Specifies the maximum number of characters to read, not counting the terminating null character.  
  
 `rString`  
 A reference to a `CString` object that will contain the string when the function returns.  
  
## Return Value  
 A pointer to the buffer containing the text data. **NULL** if end-of-file was reached without reading any data; or if boolean, **FALSE** if end-of-file was reached without reading any data.  
  
## Remarks  
 Reading is stopped by the first newline character. If, in that case, fewer than `nMax`–1 characters have been read, a newline character is stored in the buffer. A null character ('\0') is appended in either case.  
  
 [CFile::Read](../vs140/CFile--Read.md) is also available for text-mode input, but it does not terminate on a carriage return–linefeed pair.  
  
> [!NOTE]
>  The `CString` version of this function removes the `'\n'` if present; the `LPTSTR` version does not.  
  
## Example  
 [!CODE [NVC_MFCFiles#38](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#38)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CStdioFile Class](../vs140/CStdioFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStdioFile::WriteString](../vs140/CStdioFile--WriteString.md)   
 [CFile::Read](../vs140/CFile--Read.md)