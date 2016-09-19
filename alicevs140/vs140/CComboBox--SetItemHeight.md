---
title: "CComboBox::SetItemHeight"
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
ms.assetid: 97f33f2f-e876-47b9-be12-77835bb1a1e5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetItemHeight
Call the `SetItemHeight` member function to set the height of list items in a combo box or the height of the edit-control (or static-text) portion of a combo box.  
  
## Syntax  
  
```  
  
      int SetItemHeight(  
   int nIndex,  
   UINT cyItemHeight   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies whether the height of list items or the height of the edit-control (or static-text) portion of the combo box is set.  
  
 If the combo box has the [CBS_OWNERDRAWVARIABLE](../vs140/Combo-Box-Styles.md) style, `nIndex` specifies the zero-based index of the list item whose height is to be set; otherwise, `nIndex` must be 0 and the height of all list items will be set.  
  
 If `nIndex` is –1, the height of the edit-control or static-text portion of the combo box is to be set.  
  
 `cyItemHeight`  
 Specifies the height, in pixels, of the combo-box component identified by `nIndex`.  
  
## Return Value  
 **CB_ERR** if the index or height is invalid; otherwise 0.  
  
## Remarks  
 The height of the edit-control (or static-text) portion of the combo box is set independently of the height of the list items. An application must ensure that the height of the edit-control (or static-text) portion is not smaller than the height of a particular list-box item.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#38](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#38)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetItemHeight](../vs140/CComboBox--GetItemHeight.md)   
 [WM_MEASUREITEM](http://msdn.microsoft.com/library/windows/desktop/bb775925)   
 [CB_SETITEMHEIGHT](http://msdn.microsoft.com/library/windows/desktop/bb775911)