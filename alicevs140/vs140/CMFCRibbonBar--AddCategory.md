---
title: "CMFCRibbonBar::AddCategory"
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
ms.assetid: 50ae3e36-74a4-4a3c-8f55-bd4273a2a3ed
caps.latest.revision: 23
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBar::AddCategory
Creates and initializes a new ribbon category for the ribbon bar.  
  
## Syntax  
  
```  
CMFCRibbonCategory* AddCategory(  
   LPCTSTR lpszName,  
   UINT uiSmallImagesResID,  
   UINT uiLargeImagesResID,  
   CSize sizeSmallImage = CSize(16, 16),  
   CSize sizeLargeImage = CSize(32, 32),  
   int nInsertAt = -1,  
   CRuntimeClass* pRTI = NULL   
);  
```  
  
#### Parameters  
 [in] `lpszName`  
 Name of the ribbon category.  
  
 [in] `uiSmallImagesResID`  
 Resource ID of the small image list for the ribbon category.  
  
 [in] `uiLargeImagesResID`  
 Resource ID of the large image list for the ribbon category.  
  
 [in] `sizeSmallImage`  
 Specifies the size of small images for the ribbon category.  
  
 [in] `sizeLargeImage`  
 Specifies the size of large images for the ribbon category.  
  
 [in] `nInsertAt`  
 Zero based index of the category location.  
  
 [in] `pRTI`  
 Pointer to a [CMFCRibbonCategory](../vs140/CMFCRibbonCategory-Class.md) run-time class to dynamically create a ribbon category at run-time.  
  
## Return Value  
 A pointer to the new ribbon category if the method was successful; otherwise, `NULL`.  
  
## Remarks  
 If the `pRTI` parameter is not `NULL`, the new ribbon category is created dynamically using the run-time class.  
  
## Example  
 The following example demonstrates how to use the `AddCategory` method in the `CMFCRibbonBar` class.  
  
 [!CODE [NVC_MFC_RibbonApp#5](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#5)]  
  
## Requirements  
 **Header:** afxribbonbar.h  
  
## See Also  
 [CMFCRibbonBar Class](../vs140/CMFCRibbonBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)