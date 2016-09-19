---
title: "CComboBox::GetItemHeight"
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
ms.assetid: 669a9cfd-05cd-460f-b7d3-e80fa921fafa
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetItemHeight
Call the `GetItemHeight` member function to retrieve the height of list items in a combo box.  
  
## Syntax  
  
```  
  
      int GetItemHeight(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the component of the combo box whose height is to be retrieved. If the `nIndex` parameter is –1, the height of the edit-control (or static-text) portion of the combo box is retrieved. If the combo box has the [CBS_OWNERDRAWVARIABLE](../vs140/Combo-Box-Styles.md) style, `nIndex` specifies the zero-based index of the list item whose height is to be retrieved. Otherwise, `nIndex` should be set to 0.  
  
## Return Value  
 The height, in pixels, of the specified item in a combo box. The return value is **CB_ERR** if an error occurs.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#23](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#23)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetItemHeight](../vs140/CComboBox--SetItemHeight.md)   
 [WM_MEASUREITEM](http://msdn.microsoft.com/library/windows/desktop/bb775925)   
 [CB_GETITEMHEIGHT](http://msdn.microsoft.com/library/windows/desktop/bb775860)