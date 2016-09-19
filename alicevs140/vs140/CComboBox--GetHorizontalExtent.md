---
title: "CComboBox::GetHorizontalExtent"
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
ms.assetid: 50ab291d-3f24-46c8-93e4-04e2326e0077
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetHorizontalExtent
Retrieves from the combo box the width in pixels by which the list-box portion of the combo box can be scrolled horizontally.  
  
## Syntax  
  
```  
  
UINT GetHorizontalExtent( ) const;  
  
```  
  
## Return Value  
 The scrollable width of the list-box portion of the combo box, in pixels.  
  
## Remarks  
 This is applicable only if the list-box portion of the combo box has a horizontal scroll bar.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#20)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::SetHorizontalExtent](../vs140/CListBox--SetHorizontalExtent.md)   
 [CB_GETHORIZONTALEXTENT](http://msdn.microsoft.com/library/windows/desktop/bb775857)