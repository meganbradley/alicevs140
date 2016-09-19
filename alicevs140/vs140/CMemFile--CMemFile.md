---
title: "CMemFile::CMemFile"
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
ms.assetid: fedb77d2-22d1-4177-a187-bcac913bf3a4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemFile::CMemFile
The first overload opens an empty memory file.  
  
## Syntax  
  
```  
  
      CMemFile(  
   UINT nGrowBytes = 1024   
);  
CMemFile(  
   BYTE* lpBuffer,  
   UINT nBufferSize,  
   UINT nGrowBytes = 0   
);  
```  
  
#### Parameters  
 `nGrowBytes`  
 The memory allocation increment in bytes.  
  
 *lpBuffe*r  
 Pointer to a buffer that receives information of the size `nBufferSize`.  
  
 `nBufferSize`  
 An integer that specifies the size of the file buffer, in bytes.  
  
## Remarks  
 Note that the file is opened by the constructor and that you should not call [CFile::Open](../vs140/CFile--Open.md).  
  
 The second overload acts the same as if you used the first constructor and immediately called [Attach](../vs140/CMemFile--Attach.md) with the same parameters. See **Attach** for details.  
  
## Example  
 [!CODE [NVC_MFCFiles#36](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCFiles#36)]  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CMemFile Class](../vs140/CMemFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMemFile::Attach](../vs140/CMemFile--Attach.md)