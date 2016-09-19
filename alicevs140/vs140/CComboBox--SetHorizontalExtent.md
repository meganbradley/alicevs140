---
title: "CComboBox::SetHorizontalExtent"
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
ms.assetid: 5248ea78-1472-4f98-9a10-81bef0a12c12
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetHorizontalExtent
Sets the width, in pixels, by which the list-box portion of the combo box can be scrolled horizontally.  
  
## Syntax  
  
```  
  
      void SetHorizontalExtent(  
   UINT nExtent   
);  
```  
  
#### Parameters  
 *nExtent*  
 Specifies the number of pixels by which the list-box portion of the combo box can be scrolled horizontally.  
  
## Remarks  
 If the width of the list box is smaller than this value, the horizontal scroll bar will horizontally scroll items in the list box. If the width of the list box is equal to or greater than this value, the horizontal scroll bar is hidden or, if the combo box has the [CBS_DISABLENOSCROLL](../vs140/Combo-Box-Styles.md) style, disabled.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#35](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#35)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetHorizontalExtent](../vs140/CComboBox--GetHorizontalExtent.md)   
 [CB_SETHORIZONTALEXTENT](http://msdn.microsoft.com/library/windows/desktop/bb775907)