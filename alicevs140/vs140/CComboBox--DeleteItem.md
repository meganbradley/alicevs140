---
title: "CComboBox::DeleteItem"
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
ms.assetid: 3539fc14-1327-4ec7-b9c1-e0188bd8f81e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::DeleteItem
Called by the framework when the user deletes an item from an owner-draw `CComboBox` object or destroys the combo box.  
  
## Syntax  
  
```  
  
      virtual void DeleteItem(  
   LPDELETEITEMSTRUCT lpDeleteItemStruct   
);  
```  
  
#### Parameters  
 `lpDeleteItemStruct`  
 A long pointer to a Windows [DELETEITEMSTRUCT](../vs140/DELETEITEMSTRUCT-Structure.md) structure that contains information about the deleted item. See [CWnd::OnDeleteItem](../vs140/CWnd--OnDeleteItem.md) for a description of this structure.  
  
## Remarks  
 The default implementation of this function does nothing. Override this function to redraw the combo box as needed.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#8)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::CompareItem](../vs140/CComboBox--CompareItem.md)   
 [CComboBox::DrawItem](../vs140/CComboBox--DrawItem.md)   
 [CComboBox::MeasureItem](../vs140/CComboBox--MeasureItem.md)   
 [WM_DELETEITEM](http://msdn.microsoft.com/library/windows/desktop/bb761362)