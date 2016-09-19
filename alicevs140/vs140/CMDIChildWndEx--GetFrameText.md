---
title: "CMDIChildWndEx::GetFrameText"
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
ms.assetid: 4132339f-8fdf-4271-a5d2-b342dd9f6573
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMDIChildWndEx::GetFrameText
Called by the framework to retrieve the text for the MDI child window.  
  
## Syntax  
  
```  
virtual CString GetFrameText() const;  
```  
  
## Return Value  
 A string that contains the frame window text.  
  
## Remarks  
 This method is called by the framework to determine what text to display on the MDI tab that contains the MDI child frame window.  
  
 By default this method returns the window text. Override `GetFrameText` in a `CMDIChildWndEx`-derived class to customize this behavior.  
  
## Requirements  
 **Header:** afxMDIChildWndEx.h  
  
## See Also  
 [CMDIChildWndEx Class](../vs140/CMDIChildWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStringT Class](../vs140/CStringT-Class.md)