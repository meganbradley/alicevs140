---
title: "CListBox::MeasureItem"
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
ms.assetid: f7e8043a-a528-46f1-a0dd-11efce26c4ca
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::MeasureItem
Called by the framework when a list box with an owner-draw style is created.  
  
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
 By default, this member function does nothing. Override this member function and fill in the `MEASUREITEMSTRUCT` structure to inform Windows of the list-box dimensions. If the list box is created with the [LBS_OWNERDRAWVARIABLE](../vs140/List-Box-Styles.md) style, the framework calls this member function for each item in the list box. Otherwise, this member is called only once.  
  
 For further information about using the [LBS_OWNERDRAWFIXED](../vs140/List-Box-Styles.md) style in an owner-draw list box created with the `SubclassDlgItem` member function of `CWnd`, see the discussion in [Technical Note 14](../vs140/TN014--Custom-Controls.md).  
  
 See [CWnd::OnMeasureItem](../vs140/CWnd--OnMeasureItem.md) for a description of the `MEASUREITEMSTRUCT` structure**.**  
  
## Example  
 [!CODE [NVC_MFC_CListBox#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#25)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::CompareItem](../vs140/CListBox--CompareItem.md)   
 [CWnd::OnMeasureItem](../vs140/CWnd--OnMeasureItem.md)   
 [CListBox::DrawItem](../vs140/CListBox--DrawItem.md)   
 [CListBox::DeleteItem](../vs140/CListBox--DeleteItem.md)