---
title: "CEditView::GetBufferLength"
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
ms.assetid: 58a996bb-75d0-4d2f-a7ea-a7961434f42e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::GetBufferLength
Call this member function to obtain the number of characters currently in the edit control's buffer, not including the null terminator.  
  
## Syntax  
  
```  
  
UINT GetBufferLength( ) const;  
  
```  
  
## Return Value  
 The length of the string in the buffer.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::LockBuffer](../vs140/CEditView--LockBuffer.md)   
 [CEditView::UnlockBuffer](../vs140/CEditView--UnlockBuffer.md)