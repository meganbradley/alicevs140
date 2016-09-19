---
title: "CMemFile::GrowFile"
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
ms.assetid: e0edd7c8-9768-4471-bef2-5561923be3f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMemFile::GrowFile
This function is called by several of the `CMemFile` member functions.  
  
## Syntax  
  
```  
  
      virtual void GrowFile(  
   SIZE_T dwNewLen   
);  
```  
  
#### Parameters  
 `dwNewLen`  
 New size of the memory file.  
  
## Remarks  
 You can override it if you want to change how `CMemFile` grows its file. The default implementation calls [Realloc](../vs140/CMemFile--Realloc.md) to grow an existing block (or [Alloc](../vs140/CMemFile--Alloc.md) to create a memory block), allocating memory in multiples of the `nGrowBytes` value specified in the constructor or [Attach](../vs140/CMemFile--Attach.md) call.  
  
## Requirements  
 **Header:** afx.h  
  
## See Also  
 [CMemFile Class](../vs140/CMemFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMemFile::Alloc](../vs140/CMemFile--Alloc.md)   
 [CMemFile::Realloc](../vs140/CMemFile--Realloc.md)   
 [CMemFile::CMemFile](../vs140/CMemFile--CMemFile.md)   
 [CMemFile::Attach](../vs140/CMemFile--Attach.md)