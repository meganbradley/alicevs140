---
title: "CButton::DrawItem"
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
ms.assetid: 0df15d4d-6afc-498f-97ef-412bc2c13a9e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::DrawItem
Called by the framework when a visual aspect of an owner-drawn button has changed.  
  
## Syntax  
  
```  
  
      virtual void DrawItem(  
   LPDRAWITEMSTRUCT lpDrawItemStruct   
);  
```  
  
#### Parameters  
 `lpDrawItemStruct`  
 A long pointer to a [DRAWITEMSTRUCT](../vs140/DRAWITEMSTRUCT-Structure.md) structure. The structure contains information about the item to be drawn and the type of drawing required.  
  
## Remarks  
 An owner-drawn button has the **BS_OWNERDRAW** style set. Override this member function to implement drawing for an owner-drawn `CButton` object. The application should restore all graphics device interface (GDI) objects selected for the display context supplied in `lpDrawItemStruct` before the member function terminates.  
  
 Also see the [BS_](../vs140/Button-Styles.md) style values.  
  
## Example  
 [!CODE [NVC_MFC_CButton#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CButton#3)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CButton::SetButtonStyle](../vs140/CButton--SetButtonStyle.md)   
 [WM_DRAWITEM](http://msdn.microsoft.com/library/windows/desktop/bb775923)