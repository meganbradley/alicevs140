---
title: "CStdioFile::WriteString"
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
ms.assetid: 7644edf4-0750-46c7-bce2-107a21a7e11d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStdioFile::WriteString
Writes data from a buffer to the file associated with the `CStdioFile` object.  
  
## Syntax  
  
```  
  
      virtual void WriteString(  
   LPCTSTR lpsz   
);  
```  
  
#### Parameters  
 `lpsz`  
 Specifies a pointer to a buffer that contains a null-terminated string.  
  
## Remarks  
 The terminating null character (`\0`) is not written to the file. This method writes newline characters in `lpsz` to the file as a carriage return/linefeed pair.  
  
 If you want to write data that is not null-terminated to a file, use `CStdioFile::Write` or [CFile::Write](../vs140/CFile--Write.md).  
  
 This method throws a `CInvalidArgException*` if you specify `NULL` for the `lpsz` parameter.  
  
 This method throws a `CFileException*` in response to file system errors.  
  
## Example  
 [!CODE [NVC_MFCFiles#40](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#40)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CStdioFile Class](../vs140/CStdioFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive::ReadString](../vs140/CArchive--ReadString.md)   
 [CFile::Write](../vs140/CFile--Write.md)   
 [CStdioFile::ReadString](../vs140/CStdioFile--ReadString.md)