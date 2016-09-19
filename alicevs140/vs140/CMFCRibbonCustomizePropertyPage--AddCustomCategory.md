---
title: "CMFCRibbonCustomizePropertyPage::AddCustomCategory"
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
ms.assetid: 7c13faf8-9bf3-413f-9d58-b6fd1338e9d3
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonCustomizePropertyPage::AddCustomCategory
Adds a custom category to the **Commands** combo box.  
  
## Syntax  
  
```  
void AddCustomCategory(  
   LPCTSTR lpszName,  
   const CList<UINT, UINT>& lstIDS  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `lpszName`|Specifies the custom category name.|  
|[in] `lstIDS`|Contains ribbon command IDs to be shown in the custom category.|  
  
## Remarks  
 This method adds a category named `lpszName` to the **Commands** combo box. When the user selects the category, the commands specified in `lstIDS` appear in the command list.  
  
## Requirements  
 **Header:** afxribboncustomizedialog.h  
  
## See Also  
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMFCRibbonCustomizePropertyPage Class](../vs140/CMFCRibbonCustomizePropertyPage-Class.md)