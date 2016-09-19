---
title: "CPane::OnPressCloseButton"
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
ms.assetid: a4683498-922c-465d-9bf5-4533d6a5738c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::OnPressCloseButton
Called by the framework when the user presses the close button on the caption for the pane.  
  
## Syntax  
  
```  
virtual void OnPressCloseButton();  
```  
  
## Remarks  
 This method is called by the framework when a user presses the **Close** button on the pane's caption. To receive notifications about the **Close** event, you can override this method in a derived class.  
  
## Requirements  
 **Header:** afxPane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)