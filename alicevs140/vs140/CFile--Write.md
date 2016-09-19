---
title: "CFile::Write"
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
ms.assetid: 1b439e0e-277c-4d30-9a59-d881db478372
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Write
Writes data from a buffer to the file associated with the `CFile` object.  
  
## Syntax  
  
```  
  
      virtual void Write(  
   const void* lpBuf,  
   UINT nCount   
);  
```  
  
#### Parameters  
 `lpBuf`  
 A pointer to the user-supplied buffer that contains the data to be written to the file.  
  
 `nCount`  
 The number of bytes to be transferred from the buffer. For text-mode files, carriage return–linefeed pairs are counted as single characters.  
  
## Remarks  
 **Write** throws an exception in response to several conditions, including the disk-full condition.  
  
## Example  
 [!CODE [NVC_MFCFiles#16](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#16)]  
  
 In addition, see the examples for [CFile::CFile](../vs140/CFile--CFile.md) and [CFile::Open](../vs140/CFile--Open.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::Read](../vs140/CFile--Read.md)   
 [CStdioFile::WriteString](../vs140/CStdioFile--WriteString.md)