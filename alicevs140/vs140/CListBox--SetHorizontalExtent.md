---
title: "CListBox::SetHorizontalExtent"
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
ms.assetid: 6c7741c8-3006-4326-9d0f-3beba62e22fc
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetHorizontalExtent
Sets the width, in pixels, by which a list box can be scrolled horizontally.  
  
## Syntax  
  
```  
  
      void SetHorizontalExtent(  
   int cxExtent   
);  
```  
  
#### Parameters  
 *cxExtent*  
 Specifies the number of pixels by which the list box can be scrolled horizontally.  
  
## Remarks  
 If the size of the list box is smaller than this value, the horizontal scroll bar will horizontally scroll items in the list box. If the list box is as large or larger than this value, the horizontal scroll bar is hidden.  
  
 To respond to a call to `SetHorizontalExtent`, the list box must have been defined with the [WS_HSCROLL](../vs140/Window-Styles.md) style.  
  
 This member function is not useful for multicolumn list boxes. For multicolumn list boxes, call the `SetColumnWidth` member function.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#33](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#33)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetHorizontalExtent](../vs140/CListBox--GetHorizontalExtent.md)   
 [CListBox::SetColumnWidth](../vs140/CListBox--SetColumnWidth.md)   
 [LB_SETHORIZONTALEXTENT](http://msdn.microsoft.com/library/windows/desktop/bb761344)