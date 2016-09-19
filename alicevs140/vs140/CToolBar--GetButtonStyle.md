---
title: "CToolBar::GetButtonStyle"
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
ms.assetid: 795fc425-442a-4940-b2a1-ce9594bf2665
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::GetButtonStyle
Call this member function to retrieve the style of a button or separator on the toolbar.  
  
## Syntax  
  
```  
  
      UINT GetButtonStyle(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 The index of the toolbar button or separator style to be retrieved.  
  
## Return Value  
 The style of the button or separator specified by `nIndex`.  
  
## Remarks  
 A button's style determines how the button appears and how it responds to user input. See [SetButtonStyle](../vs140/CToolBar--SetButtonStyle.md) for examples of button styles.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBar::SetButtonStyle](../vs140/CToolBar--SetButtonStyle.md)