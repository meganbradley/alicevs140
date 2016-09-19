---
title: "CSharedFile::SetHandle"
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
ms.assetid: 762fe45b-f276-462b-8a4a-b9e7c62c014e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSharedFile::SetHandle
Call this function to attach a block of global memory to the `CSharedFile` object.  
  
## Syntax  
  
```  
  
      void SetHandle(  
   HGLOBAL hGlobalMemory,  
   BOOL bAllowGrow = TRUE   
);  
```  
  
#### Parameters  
 *hGlobalMemory*  
 Handle to the global memory to be attached to the `CSharedFile`.  
  
 `bAllowGrow`  
 Specifies whether the memory block is allowed to grow.  
  
## Remarks  
 If `bAllowGrow` is nonzero, the size of the memory block is increased as necessary, for example, if an attempt is made to write more bytes to the file than were allocated for the memory block.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CSharedFile Class](../vs140/CSharedFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSharedFile::CSharedFile](../vs140/CSharedFile--CSharedFile.md)   
 [CSharedFile::Detach](../vs140/CSharedFile--Detach.md)