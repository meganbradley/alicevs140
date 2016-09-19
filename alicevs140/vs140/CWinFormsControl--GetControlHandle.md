---
title: "CWinFormsControl::GetControlHandle"
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
ms.assetid: eed8e67d-6cd1-46cc-a3a2-a492edfa06d3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinFormsControl::GetControlHandle
Retrieves a handle to the Windows Forms control.  
  
## Syntax  
  
```  
inline HWND GetControlHandle( ) const;  
```  
  
## Return Value  
 Returns a handle to the Windows Forms control.  
  
## Remarks  
 `GetControlHandle` is a helper method that returns the window handle stored in the .NET Framework control properties. The window handle value is copied to [CWnd::m_hWnd](../vs140/CWnd--m_hWnd.md) during the call to [CWnd::Attach](../vs140/CWnd--Attach.md).  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [CWinFormsControl Class](../vs140/CWinFormsControl-Class.md)   
 [GetControl](../vs140/CWinFormsControl--GetControl.md)   
 [CreateManagedControl](../Topic/CWinFormsControl::CreateManagedControl.md)