---
title: "CStatusBar::GetPaneText"
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
ms.assetid: 239b5e4c-6779-4cd9-ba6e-7ad8dc2c1b23
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStatusBar::GetPaneText
Call this member function to retrieve the text that appears in a status-bar pane.  
  
## Syntax  
  
```  
  
      CString GetPaneText(  
   int nIndex   
) const;  
void GetPaneText(  
   int nIndex,  
   CString& rString   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Index of the pane whose text is to be retrieved.  
  
 `rString`  
 A reference to a [CString](../vs140/CStringT-Class.md) object that contains the text to be retrieved.  
  
## Return Value  
 A `CString` object containing the pane's text.  
  
## Remarks  
 The second form of this member function fills a `CString` object with the string text.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CStatusBar Class](../vs140/CStatusBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CStatusBar::SetPaneText](../vs140/CStatusBar--SetPaneText.md)