---
title: "CSharedFile::CSharedFile"
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
ms.assetid: 012842e3-9cce-4590-bb2f-bb9ad4096c62
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSharedFile::CSharedFile
Constructs a `CSharedFile` object and allocates memory for it.  
  
## Syntax  
  
```  
  
      CSharedFile(  
   UINT nAllocFlags = GMEM_DDESHARE | GMEM_MOVEABLE,  
   UINT nGrowBytes = 4096   
);  
```  
  
#### Parameters  
 *nAllocFlags*  
 Flags indicating how memory is to be allocated. See [GlobalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366574) for a list of valid flag values.  
  
 `nGrowBytes`  
 The memory allocation increment in bytes.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CSharedFile Class](../vs140/CSharedFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSharedFile::Detach](../vs140/CSharedFile--Detach.md)   
 [CSharedFile::SetHandle](../vs140/CSharedFile--SetHandle.md)