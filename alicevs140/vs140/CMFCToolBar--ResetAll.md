---
title: "CMFCToolBar::ResetAll"
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
ms.assetid: 0c03b7fb-0d43-4f0b-b233-1218ec9f3d12
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::ResetAll
Restores all toolbars to their original states.  
  
## Syntax  
  
```  
static void __stdcall ResetAll();  
```  
  
## Remarks  
 This method calls the [CMFCToolBar::RestoreOriginalState](../vs140/CMFCToolBar--RestoreOriginalState.md) method on each toolbar in the application that can be restored. It uses the [CMFCToolBar::CanBeRestored](../vs140/CMFCToolBar--CanBeRestored.md) method to determine whether a toolbar can be restored.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBar::RestoreOriginalState](../vs140/CMFCToolBar--RestoreOriginalState.md)   
 [CMFCToolBar::CanBeRestored](../vs140/CMFCToolBar--CanBeRestored.md)