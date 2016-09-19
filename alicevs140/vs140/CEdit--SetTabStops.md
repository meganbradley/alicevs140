---
title: "CEdit::SetTabStops"
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
ms.assetid: 08b72f27-fc29-4f75-9c04-98827c986389
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::SetTabStops
Call this function to set the tab stops in a multiple-line edit control.  
  
## Syntax  
  
```  
  
      void SetTabStops( );  
BOOL SetTabStops(  
   const int& cxEachStop   
);  
BOOL SetTabStops(  
   int nTabStops,  
   LPINT rgTabStops   
);  
```  
  
#### Parameters  
 `cxEachStop`  
 Specifies that tab stops are to be set at every `cxEachStop` dialog units.  
  
 `nTabStops`  
 Specifies the number of tab stops contained in `rgTabStops`. This number must be greater than 1.  
  
 `rgTabStops`  
 Points to an array of unsigned integers specifying the tab stops in dialog units. A dialog unit is a horizontal or vertical distance. One horizontal dialog unit is equal to one-fourth of the current dialog base width unit, and 1 vertical dialog unit is equal to one-eighth of the current dialog base height unit. The dialog base units are computed based on the height and width of the current system font. The **GetDialogBaseUnits** Windows function returns the current dialog base units in pixels.  
  
## Return Value  
 Nonzero if the tabs were set; otherwise 0.  
  
## Remarks  
 When text is copied to a multiple-line edit control, any tab character in the text will cause space to be generated up to the next tab stop.  
  
 To set tab stops to the default size of 32 dialog units, call the parameterless version of this member function. To set tab stops to a size other than 32, call the version with the `cxEachStop` parameter. To set tab stops to an array of sizes, use the version with two parameters.  
  
 This member function is only processed by multiple-line edit controls.  
  
 `SetTabStops` does not automatically redraw the edit window. If you change the tab stops for text already in the edit control, call [CWnd::InvalidateRect](../vs140/CWnd--InvalidateRect.md) to redraw the edit window.  
  
 For more information, see [EM_SETTABSTOPS](http://msdn.microsoft.com/library/windows/desktop/bb761663) and [GetDialogBaseUnits](http://msdn.microsoft.com/library/windows/desktop/ms645475) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEditView::SetTabStops](../vs140/CEditView--SetTabStops.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::InvalidateRect](../vs140/CWnd--InvalidateRect.md)