---
title: "CListBox::CompareItem"
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
ms.assetid: d704e53f-6a0c-4380-9cd2-3f647f05e0f2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::CompareItem
Called by the framework to determine the relative position of a new item in a sorted owner-draw list box.  
  
## Syntax  
  
```  
  
      virtual int CompareItem(  
   LPCOMPAREITEMSTRUCT lpCompareItemStruct   
);  
```  
  
#### Parameters  
 `lpCompareItemStruct`  
 A long pointer to a `COMPAREITEMSTRUCT` structure.  
  
## Return Value  
 Indicates the relative position of the two items described in the [COMPAREITEMSTRUCT](../vs140/COMPAREITEMSTRUCT-Structure.md) structure. It may be any of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|–1|Item 1 sorts before item 2.|  
|0|Item 1 and item 2 sort the same.|  
|1|Item 1 sorts after item 2.|  
  
 See [CWnd::OnCompareItem](../vs140/CWnd--OnCompareItem.md) for a description of the `COMPAREITEMSTRUCT` structure.  
  
## Remarks  
 By default, this member function does nothing. If you create an owner-draw list box with the **LBS_SORT** style, you must override this member function to assist the framework in sorting new items added to the list box.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#5)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_COMPAREITEM](http://msdn.microsoft.com/library/windows/desktop/bb775921)   
 [CWnd::OnCompareItem](../vs140/CWnd--OnCompareItem.md)   
 [CListBox::DrawItem](../vs140/CListBox--DrawItem.md)   
 [CListBox::MeasureItem](../vs140/CListBox--MeasureItem.md)   
 [CListBox::DeleteItem](../vs140/CListBox--DeleteItem.md)