---
title: "CMFCPropertySheet::AddTreeCategory"
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
ms.assetid: 05cd3006-755d-44f8-8850-ed98c34369e0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPropertySheet::AddTreeCategory
Adds a new node to the tree control.  
  
## Syntax  
  
```  
CMFCPropertySheetCategoryInfo* AddTreeCategory(  
   LPCTSTR lpszLabel,  
   int nIconNum=-1,  
   int nSelectedIconNum=-1,  
   const CMFCPropertySheetCategoryInfo* pParentCategory=NULL   
);  
```  
  
#### Parameters  
 [in] `lpszLabel`  
 The name of the node.  
  
 [in] `nIconNum`  
 Zero-based index of an icon, or -1 if no icon is used. The icon is displayed next to the tree control property page when the page is not selected. The default value is -1.  
  
 [in] `nSelectedIconNum`  
 Zero-based index of an icon, or -1 if no icon is used. The icon is displayed next to the tree control property page when the page is selected. The default value is -1.  
  
 [in] `pParentCategory`  
 Pointer to a parent tree node, or `NULL` to associate the specified page with the top-level node. Set this parameter with the [CMFCPropertySheet::AddTreeCategory](../vs140/CMFCPropertySheet--AddTreeCategory.md) method.  
  
## Return Value  
 A pointer to the new node in the tree control.  
  
## Remarks  
 Use this method to add a new node, which is also referred to as a category, to the tree control. To add a node, create a `CMFCPropertySheet` object, call the [CMFCPropertySheet::SetLook](../vs140/CMFCPropertySheet--SetLook.md) method with the `look` parameter set to  `CMFCPropertySheet::PropSheetLook_Tree`, and then use this method to add the node.  
  
 Use the return value of this method in subsequent calls to [CMFCPropertySheet::AddPageToTree](../vs140/CMFCPropertySheet--AddPageToTree.md) and [CMFCPropertySheet::AddTreeCategory](../vs140/CMFCPropertySheet--AddTreeCategory.md).  
  
## Requirements  
 **Header:** afxpropertysheet.h  
  
## See Also  
 [CMFCPropertySheet Class](../vs140/CMFCPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)