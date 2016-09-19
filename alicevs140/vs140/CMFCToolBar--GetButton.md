---
title: "CMFCToolBar::GetButton"
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
ms.assetid: bd6cade9-e946-45d7-9483-635c88cf29b9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetButton
Returns a pointer to the [CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md) object at a specified index.  
  
## Syntax  
  
```  
CMFCToolBarButton* GetButton(  
   int iIndex   
) const;  
```  
  
#### Parameters  
 [in] `iIndex`  
 Specifies the index of the button to return.  
  
## Return Value  
 A pointer to the toolbar button if it exists; or `NULL` if there is no such button.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)