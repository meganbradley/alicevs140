---
title: "CComboBox::GetTopIndex"
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
ms.assetid: 6776c539-b8a0-48ba-a956-2a423c3fbe5f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetTopIndex
Retrieves the zero-based index of the first visible item in the list-box portion of the combo box.  
  
## Syntax  
  
```  
  
int GetTopIndex( ) const;  
  
```  
  
## Return Value  
 The zero-based index of the first visible item in the list-box portion of the combo box if successful, **CB_ERR** otherwise.  
  
## Remarks  
 Initially, item 0 is at the top of the list box, but if the list box is scrolled, another item may be at the top.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#25](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#25)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetTopIndex](../vs140/CComboBox--SetTopIndex.md)   
 [CB_GETTOPINDEX](http://msdn.microsoft.com/library/windows/desktop/bb775871)