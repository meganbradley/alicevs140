---
title: "CMFCToolBarEditBoxButton::CMFCToolBarEditBoxButton"
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
ms.assetid: 67c5b9a4-5c0f-4679-bb90-5343fc34cd50
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarEditBoxButton::CMFCToolBarEditBoxButton
Constructs a [CMFCToolBarEditBoxButton](../vs140/CMFCToolBarEditBoxButton-Class.md) object.  
  
## Syntax  
  
```  
CMFCToolBarEditBoxButton(  
   UINT uiID,  
   int iImage,  
   DWORD dwStyle=ES_AUTOHSCROLL,  
   int iWidth=0   
);  
```  
  
#### Parameters  
 [in] `uiID`  
 Specifies the control ID.  
  
 [in] `iImage`  
 Specifies the zero-based index of a toolbar image. The image is located in the [CMFCToolBarImages](../vs140/CMFCToolBarImages-Class.md) object that [CMFCToolBar](../Topic/CMFCToolBar%20Class.md) class maintains.  
  
 [in] `dwStyle`  
 Specifies the edit control style.  
  
 [in] `iWidth`  
 Specifies the width in pixels of the edit control.  
  
## Remarks  
 The default constructor sets the edit control style to the following combination:  
  
 `WS_CHILD | WS_VISIBLE | ES_AUTOHSCROLL`  
  
 The default width of the control is 150 pixels.  
  
## Requirements  
 **Header:** afxtoolbareditboxbutton.h  
  
## See Also  
 [CMFCToolBarEditBoxButton Class](../vs140/CMFCToolBarEditBoxButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)