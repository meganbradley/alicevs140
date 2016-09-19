---
title: "CListBox::DeleteItem"
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
ms.assetid: a98483f6-b689-475b-9bc9-d87da9cc6fcd
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::DeleteItem
Called by the framework when the user deletes an item from an owner-draw `CListBox` object or destroys the list box.  
  
## Syntax  
  
```  
  
      virtual void DeleteItem(  
   LPDELETEITEMSTRUCT lpDeleteItemStruct   
);  
```  
  
#### Parameters  
 `lpDeleteItemStruct`  
 A long pointer to a Windows [DELETEITEMSTRUCT](../vs140/DELETEITEMSTRUCT-Structure.md) structure that contains information about the deleted item.  
  
## Remarks  
 The default implementation of this function does nothing. Override this function to redraw an owner-draw list box as needed.  
  
 See [CWnd::OnDeleteItem](../vs140/CWnd--OnDeleteItem.md) for a description of the `DELETEITEMSTRUCT` structure.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#6)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::CompareItem](../vs140/CListBox--CompareItem.md)   
 [CWnd::OnDeleteItem](../vs140/CWnd--OnDeleteItem.md)   
 [CListBox::DrawItem](../vs140/CListBox--DrawItem.md)   
 [CListBox::MeasureItem](../vs140/CListBox--MeasureItem.md)