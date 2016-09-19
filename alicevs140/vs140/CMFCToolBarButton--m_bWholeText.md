---
title: "CMFCToolBarButton::m_bWholeText"
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
ms.assetid: b233f90c-d1ce-44d2-810c-522cbfca3e4b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::m_bWholeText
Specifies whether the button displays its full text label even if it does not fit in the bounding rectangle.  
  
## Syntax  
  
```  
BOOL m_bWholeText;  
```  
  
## Remarks  
 If this data member is set to `TRUE`, the framework displays the full text label by enlarging the button. Otherwise, the framework truncates and appends an ellipsis (**...**) to the text label.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)