---
title: "CComboBox::CompareItem"
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
ms.assetid: ca323a36-1cf8-433e-ba76-8c54ec0050e6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::CompareItem
Called by the framework to determine the relative position of a new item in the list-box portion of a sorted owner-draw combo box.  
  
## Syntax  
  
```  
  
      virtual int CompareItem(  
   LPCOMPAREITEMSTRUCT lpCompareItemStruct   
);  
```  
  
#### Parameters  
 `lpCompareItemStruct`  
 A long pointer to a [COMPAREITEMSTRUCT](../vs140/COMPAREITEMSTRUCT-Structure.md) structure.  
  
## Return Value  
 Indicates the relative position of the two items described in the `COMPAREITEMSTRUCT` structure. It can be any of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|– 1|Item 1 sorts before item 2.|  
|0|Item 1 and item 2 sort the same.|  
|1|Item 1 sorts after item 2.|  
  
 See [CWnd::OnCompareItem](../vs140/CWnd--OnCompareItem.md) for a description of `COMPAREITEMSTRUCT`.  
  
## Remarks  
 By default, this member function does nothing. If you create an owner-draw combo box with the **LBS_SORT** style, you must override this member function to assist the framework in sorting new items added to the list box.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#5)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_COMPAREITEM](http://msdn.microsoft.com/library/windows/desktop/bb775921)   
 [CComboBox::DrawItem](../vs140/CComboBox--DrawItem.md)   
 [CComboBox::MeasureItem](../vs140/CComboBox--MeasureItem.md)   
 [CComboBox::DeleteItem](../vs140/CComboBox--DeleteItem.md)