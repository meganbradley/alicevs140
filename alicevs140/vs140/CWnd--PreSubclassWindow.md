---
title: "CWnd::PreSubclassWindow"
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
ms.assetid: 3a85e9a4-9276-4d41-aba7-26a1260a3051
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::PreSubclassWindow
This member function is called by the framework to allow other necessary subclassing to occur before the window is subclassed.  
  
## Syntax  
  
```  
  
virtual void PreSubclassWindow( );  
  
```  
  
## Remarks  
 Overriding this member function allows for dynamic subclassing of controls. It is an advanced overridable.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SubclassWindow](../vs140/CWnd--SubclassWindow.md)   
 [CWnd::UnsubclassWindow](../vs140/CWnd--UnsubclassWindow.md)   
 [CWnd::DefWindowProc](../vs140/CWnd--DefWindowProc.md)   
 [CWnd::SubclassDlgItem](../vs140/CWnd--SubclassDlgItem.md)   
 [CWnd::Attach](../vs140/CWnd--Attach.md)   
 [CWnd::PreCreateWindow](../vs140/CWnd--PreCreateWindow.md)