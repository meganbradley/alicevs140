---
title: "CArchive::WriteString"
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
ms.assetid: 9b48db3f-3b79-4796-af3f-60778ae5c39b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CArchive::WriteString
Use this member function to write data from a buffer to the file associated with the `CArchive` object.  
  
## Syntax  
  
```  
  
      void WriteString(  
   LPCTSTR lpsz   
);  
```  
  
#### Parameters  
 `lpsz`  
 Specifies a pointer to a buffer containing a null-terminated text string.  
  
## Remarks  
 The terminating null character ('\0') is not written to the file; nor is a newline automatically written.  
  
 `WriteString` throws an exception in response to several conditions, including the disk-full condition.  
  
 **Write** is also available, but rather than terminating on a null character, it writes the requested number of bytes to the file.  
  
## Example  
 [!CODE [NVC_MFCSerialization#30](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCSerialization#30)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)