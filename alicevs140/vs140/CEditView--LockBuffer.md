---
title: "CEditView::LockBuffer"
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
ms.assetid: f5f21c68-97d2-433f-b3f6-800627ca870f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::LockBuffer
Call this member function to obtain a pointer to the buffer. The buffer should not be modified.  
  
## Syntax  
  
```  
  
LPCTSTR LockBuffer( ) const;  
  
```  
  
## Return Value  
 A pointer to the edit control's buffer.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEditView::UnlockBuffer](../vs140/CEditView--UnlockBuffer.md)   
 [CEditView::GetBufferLength](../vs140/CEditView--GetBufferLength.md)