---
title: "CMFCRibbonApplicationButton::SetImage"
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
ms.assetid: d9659fd5-64ea-4bfd-814a-b006fb6b92c5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonApplicationButton::SetImage
Assigns an image to the application button.  
  
## Syntax  
  
```  
void SetImage(  
   UINT uiBmpResID   
);  
void SetImage(  
   HBITMAP hBmp   
);  
```  
  
#### Parameters  
 [in] `uiBmpResID`  
 The resource ID of the image to display on the application button.  
  
 [in] `hBmp`  
 A handle to a bitmap to display on the application button.  
  
## Remarks  
 Use this method to assign a new image to the ribbon application button after you create the button. The application button is located in the upper-left corner of the application window.  
  
## Requirements  
 **Header:** afxRibbonBar.h  
  
## See Also  
 [CMFCRibbonApplicationButton Class](../vs140/CMFCRibbonApplicationButton-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)