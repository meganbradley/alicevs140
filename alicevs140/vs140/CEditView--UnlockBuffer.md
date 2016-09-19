---
title: "CEditView::UnlockBuffer"
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
ms.assetid: b77a07e1-d63d-4ee0-9a86-4f74c8ddcc9d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::UnlockBuffer
Call this member function to unlock the buffer.  
  
## Syntax  
  
```  
  
void UnlockBuffer( ) const;  
  
```  
  
## Remarks  
 Call `UnlockBuffer` after you have finished using the pointer returned by [LockBuffer](../vs140/CEditView--LockBuffer.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::LockBuffer](../vs140/CEditView--LockBuffer.md)   
 [CEditView::GetBufferLength](../vs140/CEditView--GetBufferLength.md)