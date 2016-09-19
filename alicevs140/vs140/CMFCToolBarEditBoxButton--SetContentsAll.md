---
title: "CMFCToolBarEditBoxButton::SetContentsAll"
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
ms.assetid: a067c394-cd56-442c-853b-c9f38f02d409
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::SetContentsAll
Finds a [CMFCToolBarEditBoxButton](../vs140/CMFCToolBarEditBoxButton-Class.md) object that has a specified command ID and sets the specified text within its text box.  
  
## Syntax  
  
```  
static BOOL SetContentsAll(  
   UINT uiCmd,  
   const CString& strContents   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 Specifies the command ID of the control for which the text will be changed.  
  
 [in] `strContents`  
 Specifies the new text to set.  
  
## Return Value  
 Nonzero if the text was set; 0 if the `CMFCToolBarEditBoxButton` control with the specified command ID does not exist.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)