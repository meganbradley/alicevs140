---
title: "CSyncObject::operator HANDLE"
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
ms.assetid: 92990e01-7577-404c-8770-41c6b38b2a77
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSyncObject::operator HANDLE
Use this operator to get the handle of the `CSyncObject` object.  
  
## Syntax  
  
```  
  
operator HANDLE( ) const;  
  
```  
  
## Return Value  
 If successful, the handle of the synchronization object; otherwise, **NULL**.  
  
## Remarks  
 You can use the handle to call Windows APIs directly.  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CSyncObject Class](../vs140/CSyncObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)