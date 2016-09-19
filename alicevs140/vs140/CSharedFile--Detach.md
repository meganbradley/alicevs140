---
title: "CSharedFile::Detach"
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
ms.assetid: 23c0d60e-771a-4676-af38-0ec7eb2f266a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSharedFile::Detach
Call this function to close the memory file and detach it from the memory block.  
  
## Syntax  
  
```  
  
HGLOBAL Detach( );  
  
```  
  
## Return Value  
 The handle of the memory block that contains the contents of the memory file.  
  
## Remarks  
 You can reopen it by calling [SetHandle](../vs140/CSharedFile--SetHandle.md), using the handle returned by **Detach**.  
  
## Requirements  
 **Header:** afxadv.h  
  
## See Also  
 [CSharedFile Class](../vs140/CSharedFile-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSharedFile::CSharedFile](../vs140/CSharedFile--CSharedFile.md)   
 [CSharedFile::SetHandle](../vs140/CSharedFile--SetHandle.md)