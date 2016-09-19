---
title: "CComboBox::SetTopIndex"
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
ms.assetid: 38f789a1-466d-4d08-839c-0d44a2f77935
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::SetTopIndex
Ensures that a particular item is visible in the list-box portion of the combo box.  
  
## Syntax  
  
```  
  
      int SetTopIndex(  
   int nIndex   
);  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the zero-based index of the list-box item.  
  
## Return Value  
 Zero if successful, or **CB_ERR** if an error occurs.  
  
## Remarks  
 The system scrolls the list box until either the item specified by `nIndex` appears at the top of the list box or the maximum scroll range has been reached.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#40](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#40)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::GetTopIndex](../vs140/CComboBox--GetTopIndex.md)   
 [CB_SETTOPINDEX](http://msdn.microsoft.com/library/windows/desktop/bb775917)