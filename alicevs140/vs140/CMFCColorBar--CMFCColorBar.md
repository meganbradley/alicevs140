---
title: "CMFCColorBar::CMFCColorBar"
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
ms.assetid: 1ce462a4-7319-4dda-b260-0e7377da7379
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorBar::CMFCColorBar
Constructs a `CMFCColorBar` object.  
  
## Syntax  
  
```  
CMFCColorBar(  
   const CArray<COLORREF,COLORREF>& colors,  
   COLORREF color,  
   LPCTSTR lpszAutoColor,  
   LPCTSTR lpszOtherColor,  
   LPCTSTR lpszDocColors,  
   CList<COLORREF,COLORREF>& lstDocColors,  
   int nColumns,  
   int nRowsDockHorz,  
   int nColDockVert,  
   COLORREF colorAutomatic,  
   UINT nCommandID,  
   CMFCColorButton* pParentBtn   
);  
CMFCColorBar(  
   const CArray<COLORREF,COLORREF>& colors,  
   COLORREF color,  
   LPCTSTR lpszAutoColor,  
   LPCTSTR lpszOtherColor,  
   LPCTSTR lpszDocColors,  
   CList<COLORREF,COLORREF>& lstDocColors,  
   int nColumns,  
   COLORREF colorAutomatic,  
   UINT nCommandID,  
   CMFCRibbonColorButton* pParentRibbonBtn   
);  
CMFCColorBar(  
   CMFCColorBar& src,  
   UINT uiCommandID   
);  
```  
  
#### Parameters  
 [in] `colors`  
 An array of colors that the framework displays on the color bar control.  
  
 [in] `color`  
 The initially selected color.  
  
 [in] `lpszAutoColor`  
 The text label of the *automatic* (default) color button, or `NULL`.  
  
 The standard label for the automatic button is **Automatic**.  
  
 [in] `lpszOtherColor`  
 The text label of the *other* button, which displays more color choices, or `NULL`.  
  
 The standard label for the other button is **More Colors...**.  
  
 [in] `lpszDocColors`  
 The text label of the document colors button. The document colors palette lists all the colors that the document currently uses.  
  
 [in] `lstDocColors`  
 A list of colors that the document currently uses.  
  
 [in] `nColumns`  
 The number of columns that the array of colors has.  
  
 [in] `nRowsDockHorz`  
 The number of rows that the color bar has when it is docked horizontally.  
  
 [in] `nColDockVert`  
 The number of columns that the color bar has when it is docked vertically.  
  
 [in] `colorAutomatic`  
 The default color that the framework applies when you click the automatic button.  
  
 [in] `nCommandID`  
 The color bar control command ID.  
  
 [in] `pParentBtn`  
 A pointer to a parent button.  
  
 [in] `src`  
 An existing `CMFCColorBar` object to be copied into the new `CMFCColorBar` object.  
  
 [in] `uiCommandID`  
 The command ID.  
  
## Requirements  
 **Header:** afxcolorbar.h  
  
## See Also  
 [CMFCColorBar Class](../vs140/CMFCColorBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)   
 [CMFCColorBar::Create](../vs140/CMFCColorBar--Create.md)