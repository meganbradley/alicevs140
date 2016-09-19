---
title: "CMFCVisualManager::OnUpdateSystemColors"
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
ms.assetid: b73be6e7-4da6-4e2a-a0d9-8f4f4ca5a0b8
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnUpdateSystemColors
The framework calls this function when it changes the system colors.  
  
## Syntax  
  
```  
virtual void OnUpdateSystemColors();  
```  
  
## Remarks  
 The framework calls this method as a part of processing the `WM_SYSCOLORCHANGE` message. The default implementation does nothing. Override this method in a derived visual manager if you want to execute custom code when the colors change in your application.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)