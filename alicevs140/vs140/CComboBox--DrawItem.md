---
title: "CComboBox::DrawItem"
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
ms.assetid: b1148873-a8db-4bbc-9b4b-70ccb778b765
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::DrawItem
Called by the framework when a visual aspect of an owner-draw combo box changes.  
  
## Syntax  
  
```  
  
      virtual void DrawItem(  
   LPDRAWITEMSTRUCT lpDrawItemStruct   
);  
```  
  
#### Parameters  
 `lpDrawItemStruct`  
 A pointer to a [DRAWITEMSTRUCT](../vs140/DRAWITEMSTRUCT-Structure.md) structure that contains information about the type of drawing required.  
  
## Remarks  
 The **itemAction** member of the `DRAWITEMSTRUCT` structure defines the drawing action that is to be performed. See [CWnd::OnDrawItem](../vs140/CWnd--OnDrawItem.md) for a description of this structure.  
  
 By default, this member function does nothing. Override this member function to implement drawing for an owner-draw `CComboBox` object. Before this member function terminates, the application should restore all graphics device interface (GDI) objects selected for the display context supplied in `lpDrawItemStruct`.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#11)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::CompareItem](../vs140/CComboBox--CompareItem.md)   
 [WM_DRAWITEM](http://msdn.microsoft.com/library/windows/desktop/bb775923)   
 [CComboBox::MeasureItem](../vs140/CComboBox--MeasureItem.md)   
 [CComboBox::DeleteItem](../vs140/CComboBox--DeleteItem.md)