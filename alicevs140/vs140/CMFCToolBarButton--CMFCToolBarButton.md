---
title: "CMFCToolBarButton::CMFCToolBarButton"
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
ms.assetid: c2e46af4-5859-40fb-bf11-85497a78ebdc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::CMFCToolBarButton
Constructs and initializes a `CMFCToolBarButton` object.  
  
## Syntax  
  
```  
CMFCToolBarButton(  
   UINT uiID,  
   int iImage,  
   LPCTSTR lpszText=NULL,  
   BOOL bUserButton=FALSE,  
   BOOL bLocked=FALSE  
);  
```  
  
#### Parameters  
 [in] `uiID`  
 The command ID of the button.  
  
 [in] `iImage`  
 The image index of the button in the collection of images.  
  
 [in] `lpszText`  
 The text label of the button. Can be `NULL`.  
  
 [in] `bUserButton`  
 A Boolean value that determines whether the button is user-defined. If this parameter is `TRUE`, the button is user-defined. Otherwise, the button image is loaded from a resource.  
  
 [in] `bLocked`  
 A Boolean value that determines whether the button can be customized. If this parameter is `TRUE`, the button cannot be customized. Otherwise, the button can be customized.  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)