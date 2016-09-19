---
title: "CMFCRibbonEdit::GetTextAlign"
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
ms.assetid: aa40a5f5-f19f-423a-8bb9-35a9e98444e6
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::GetTextAlign
Retrieves the alignment of the text in the text box.  
  
## Syntax  
  
```  
int GetTextAlign() const;  
```  
  
## Return Value  
 A text alignment enumerated value. See the Remarks section for possible values.  
  
## Remarks  
 The returned value is one of the following edit control styles:  
  
-   **ES_LEFT** for left alignment  
  
-   **ES_CENTER** for center alignment  
  
-   **ES_RIGHT** for right alignment  
  
 For more information about these styles, see [Edit Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb775464).  
  
## Requirements  
 **Header:** afxRibbonEdit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)