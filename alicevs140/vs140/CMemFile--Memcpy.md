---
title: "CMemFile::Memcpy"
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
ms.assetid: 4ee8e96e-df1a-43cc-91a4-26f6396f1519
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemFile::Memcpy
This function is called by the `CMemFile` overrides of [CFile::Read](../vs140/CFile--Read.md) and [CFile::Write](../vs140/CFile--Write.md) to transfer data to and from the memory file.  
  
## Syntax  
  
```  
  
   virtual BYTE* Memcpy(   
BYTE* lpMemTarget,   
const BYTE* lpMemSource,   
SIZE_T nBytes);  
```  
  
#### Parameters  
 `lpMemTarget`  
 Pointer to the memory block into which the source memory will be copied.  
  
 `lpMemSource`  
 Pointer to the source memory block.  
  
 `nBytes`  
 Number of bytes to be copied.  
  
## Return Value  
 A copy of `lpMemTarget`.  
  
## Remarks  
 Override this function if you want to change the way that `CMemFile` does these memory copies.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CMemFile Class](../vs140/CMemFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFile::Read](../vs140/CFile--Read.md)   
 [CFile::Write](../vs140/CFile--Write.md)