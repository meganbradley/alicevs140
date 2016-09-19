---
title: "CMFCRibbonEdit::SetTextAlign"
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
ms.assetid: caa01f73-930f-4e41-9e0d-514378575736
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::SetTextAlign
Sets the text alignment of the text box.  
  
## Syntax  
  
```  
void SetTextAlign(  
    int nAlign   
);  
```  
  
#### Parameters  
 [in] `nAlign`  
 A text alignment enumerated value. See the Remarks section for possible values.  
  
## Remarks  
 The parameter `nAlign` is one of the following edit control styles:  
  
-   **ES_LEFT** for left alignment  
  
-   **ES_CENTER** for center alignment  
  
-   **ES_RIGHT** for right alignment  
  
 For more information about these styles, see [Edit Control Styles](http://msdn.microsoft.com/library/windows/desktop/bb775464).  
  
## Requirements  
 **Header:** afxRibbonEdit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)