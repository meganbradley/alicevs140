---
title: "CFile::Read"
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
ms.assetid: 72afe77e-8a6f-4308-8c1a-3899ad4f8a36
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFile::Read
Reads data into a buffer from the file associated with the `CFile` object.  
  
## Syntax  
  
```  
  
      virtual UINT Read(  
   void* lpBuf,  
   UINT nCount   
);  
```  
  
#### Parameters  
 `lpBuf`  
 Pointer to the user-supplied buffer that is to receive the data read from the file.  
  
 `nCount`  
 The maximum number of bytes to be read from the file. For text-mode files, carriage return–linefeed pairs are counted as single characters.  
  
## Return Value  
 The number of bytes transferred to the buffer. Note that for all `CFile` classes, the return value may be less than `nCount` if the end of file was reached.  
  
## Example  
 [!CODE [NVC_MFCFiles#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#15)]  
  
 For another example see [CFile::Open](../vs140/CFile--Open.md).  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CFile Class](../vs140/CFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)