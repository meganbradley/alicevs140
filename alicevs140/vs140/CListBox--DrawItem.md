---
title: "CListBox::DrawItem"
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
ms.assetid: c52c84dc-4cae-4a5e-991f-5a9a5a584f7e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::DrawItem
Called by the framework when a visual aspect of an owner-draw list box changes.  
  
## Syntax  
  
```  
  
      virtual void DrawItem(  
   LPDRAWITEMSTRUCT lpDrawItemStruct   
);  
```  
  
#### Parameters  
 `lpDrawItemStruct`  
 A long pointer to a [DRAWITEMSTRUCT](../vs140/DRAWITEMSTRUCT-Structure.md) structure that contains information about the type of drawing required.  
  
## Remarks  
 The **itemAction** and **itemState** members of the `DRAWITEMSTRUCT` structure define the drawing action that is to be performed.  
  
 By default, this member function does nothing. Override this member function to implement drawing for an owner-draw `CListBox` object. The application should restore all graphics device interface (GDI) objects selected for the display context supplied in `lpDrawItemStruct` before this member function terminates.  
  
 See [CWnd::OnDrawItem](../vs140/CWnd--OnDrawItem.md) for a description of the `DRAWITEMSTRUCT` structure.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#9)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::CompareItem](../vs140/CListBox--CompareItem.md)   
 [CWnd::OnDrawItem](../vs140/CWnd--OnDrawItem.md)   
 [WM_DRAWITEM](http://msdn.microsoft.com/library/windows/desktop/bb775923)   
 [CListBox::MeasureItem](../vs140/CListBox--MeasureItem.md)   
 [CListBox::DeleteItem](../vs140/CListBox--DeleteItem.md)