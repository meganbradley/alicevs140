---
title: "CMFCToolBar::GetButtonStyle"
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
ms.assetid: 1ad59283-0020-4048-a347-8716df3e98b3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetButtonStyle
Returns the current style of the toolbar button that is located at the specified index.  
  
## Syntax  
  
```  
UINT GetButtonStyle(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 [in] `nIndex`  
 Specifies the index of a toolbar button.  
  
## Return Value  
 A value that specifies the style of the toolbar button. . See [ToolBar Control Styles](../vs140/ToolBar-Control-Styles.md) for a list of possible styles.  
  
## Remarks  
 Call [CMFCToolBar::SetButtonStyle](../vs140/CMFCToolBar--SetButtonStyle.md) to set the style of a toolbar button  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)