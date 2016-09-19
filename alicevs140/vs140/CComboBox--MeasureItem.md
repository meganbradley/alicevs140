---
title: "CComboBox::MeasureItem"
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
ms.assetid: 389f0d45-b443-4de2-ab13-a58aaad90d87
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::MeasureItem
Called by the framework when a combo box with an owner-draw style is created.  
  
## Syntax  
  
```  
  
      virtual void MeasureItem(  
   LPMEASUREITEMSTRUCT lpMeasureItemStruct   
);  
```  
  
#### Parameters  
 `lpMeasureItemStruct`  
 A long pointer to a [MEASUREITEMSTRUCT](../vs140/MEASUREITEMSTRUCT-Structure.md) structure.  
  
## Remarks  
 By default, this member function does nothing. Override this member function and fill in the `MEASUREITEMSTRUCT` structure to inform Windows of the dimensions of the list box in the combo box. If the combo box is created with the [CBS_OWNERDRAWVARIABLE](../vs140/Combo-Box-Styles.md) style, the framework calls this member function for each item in the list box. Otherwise, this member is called only once.  
  
 Using the **CBS_OWNERDRAWFIXED** style in an owner-draw combo box created with the [SubclassDlgItem](../vs140/CWnd--SubclassDlgItem.md) member function of `CWnd` involves further programming considerations. See the discussion in [Technical Note 14](../vs140/TN014--Custom-Controls.md).  
  
 See [CWnd::OnMeasureItem](../vs140/CWnd--OnMeasureItem.md) for a description of the `MEASUREITEMSTRUCT` structure.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#29](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#29)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::CompareItem](../vs140/CComboBox--CompareItem.md)   
 [CComboBox::DrawItem](../vs140/CComboBox--DrawItem.md)   
 [WM_MEASUREITEM](http://msdn.microsoft.com/library/windows/desktop/bb775925)   
 [CComboBox::DeleteItem](../vs140/CComboBox--DeleteItem.md)