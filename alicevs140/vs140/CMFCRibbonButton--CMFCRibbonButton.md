---
title: "CMFCRibbonButton::CMFCRibbonButton"
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
ms.assetid: 14f0f5a1-fc94-44d9-b8d0-001609085bde
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonButton::CMFCRibbonButton
Constructs a ribbon button object.  
  
## Syntax  
  
```  
CMFCRibbonButton(  
   UINT nID,  
   LPCTSTR lpszText,  
   int nSmallImageIndex=-1,  
   int nLargeImageIndex=-1,  
   BOOL bAlwaysShowDescription=FALSE   
);  
CMFCRibbonButton(  
   UINT nID,  
   LPCTSTR lpszText,  
   HICON hIcon,  
   BOOL bAlwaysShowDescription=FALSE,  
   HICON hIconSmall=NULL,  
   BOOL bAutoDestroyIcon=FALSE,  
   BOOL bAlphaBlendIcon=FALSE   
);  
```  
  
#### Parameters  
 [in] `nID`  
 Specifies the command ID of the button.  
  
 [in] `lpszText`  
 Specifies the text label of the button.  
  
 [in] `nSmallImageIndex`  
 Specifies a zero-based index of the button's small image in the image list of the parent category.  
  
 [in] `nLargeImageIndex`  
 Specifies a zero-based index of the button's large image in the image list of the parent category.  
  
 [in] `hIcon`  
 Specifies a handle to the icon that the application uses as the button's image.  
  
## Example  
 The following example demonstrates how to construct a `CMFCRibbonButton` object.  
  
 [!CODE [NVC_MFC_RibbonApp#6](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#6)]  
  
## Requirements  
 **Header:** afxribbonbutton.h  
  
## See Also  
 [CMFCRibbonButton Class](../vs140/CMFCRibbonButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)