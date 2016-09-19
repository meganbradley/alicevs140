---
title: "CWnd::PostNcDestroy"
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
ms.assetid: ecdb0263-0b5b-4ce6-8128-025f2fc6c54b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::PostNcDestroy
Called by the default [OnNcDestroy](../vs140/CWnd--OnNcDestroy.md) member function after the window has been destroyed.  
  
## Syntax  
  
```  
  
virtual void PostNcDestroy( );  
```  
  
## Remarks  
 Derived classes can use this function for custom cleanup such as the deletion of the **this** pointer.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::OnNcDestroy](../vs140/CWnd--OnNcDestroy.md)