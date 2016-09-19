---
title: "CMenu::DrawItem"
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
ms.assetid: bd0c399f-8069-4276-b992-c12dafda6d0a
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMenu::DrawItem
Called by the framework when a visual aspect of an owner-drawn menu changes.  
  
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
 The `itemAction` member of the `DRAWITEMSTRUCT` structure defines the drawing action that is to be performed. Override this member function to implement drawing for an owner-draw `CMenu` object. The application should restore all graphics device interface (GDI) objects selected for the display context supplied in `lpDrawItemStruct` before the termination of this member function.  
  
 See [CWnd::OnDrawItem](../vs140/CWnd--OnDrawItem.md) for a description of the `DRAWITEMSTRUCT` structure.  
  
## Example  
 The following code is from the MFC [CTRLTEST](../vs140/Visual-C---Samples.md) sample:  
  
 [!CODE [NVC_MFCWindowing#24](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#24)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMenu Class](../vs140/CMenu-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)