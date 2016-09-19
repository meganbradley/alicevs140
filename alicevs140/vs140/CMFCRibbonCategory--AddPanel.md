---
title: "CMFCRibbonCategory::AddPanel"
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
ms.assetid: b92994b8-47d5-4e04-bb30-ada6514fcc40
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCategory::AddPanel
Creates a ribbon panel for the ribbon category.  
  
## Syntax  
  
```  
CMFCRibbonPanel* AddPanel(  
   LPCTSTR lpszPanelName,  
   HICON hIcon = 0,  
   CRuntimeClass* pRTI = NULL   
);  
```  
  
#### Parameters  
 [in] `lpszPanelName`  
 Pointer to the name of the new ribbon panel.  
  
 [in] `hIcon`  
 Handle to the default icon for the new ribbon panel.  
  
 [in] `pRTI`  
 Pointer to runtime class information for a custom ribbon panel.  
  
## Return Value  
 Pointer to the new ribbon panel if the method was successful; otherwise `NULL` if the panel was not created.  
  
## Remarks  
 If you want to create a custom ribbon panel, you must specify its runtime class information in `pRTI`. The custom ribbon panel class must be derived from the `CMFCRibbonPanel` class.  
  
 The default icon for the ribbon panel is displayed when there is insufficient space to display the ribbon elements.  
  
## Example  
 The following example demonstrates how to use the `AddPanel` method in the `CMFCRibbonCategory` class.  
  
 [!CODE [NVC_MFC_RibbonApp#10](../CodeSnippet/VS_Snippets_Misc/NVC_MFC_RibbonApp#10)]  
  
## Requirements  
 **Header:** afxribboncategory.h  
  
## See Also  
 [CMFCRibbonCategory Class](../vs140/CMFCRibbonCategory-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)