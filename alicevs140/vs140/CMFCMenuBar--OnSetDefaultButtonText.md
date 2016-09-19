---
title: "CMFCMenuBar::OnSetDefaultButtonText"
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
ms.assetid: 9010a1f3-ee53-4d24-bb39-8ec2b81a0259
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCMenuBar::OnSetDefaultButtonText
The framework calls this method when the user changes the text of an item on the menu bar.  
  
## Syntax  
  
```  
virtual BOOL OnSetDefaultButtonText(  
   CMFCToolBarButton* pButton  
);  
```  
  
#### Parameters  
 [in] `pButton`  
 A pointer to the [CMFCToolBarButton](../vs140/CMFCToolBarButton-Class.md) object that the user wants to customize.  
  
## Return Value  
 `TRUE` if the framework applies the user changes to the menu bar; otherwise `FALSE`.  
  
## Remarks  
 The default implementation for this method changes the text of the button to the text that the user provides.  
  
## Requirements  
 **Header:** afxmenubar.h  
  
## See Also  
 [CMFCMenuBar Class](../vs140/CMFCMenuBar-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)