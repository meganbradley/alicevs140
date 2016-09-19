---
title: "CDialog::MapDialogRect"
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
ms.assetid: 5c260147-4ba2-4d93-a7e8-708b83c212bb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::MapDialogRect
Call to convert the dialog-box units of a rectangle to screen units.  
  
## Syntax  
  
```  
  
      void MapDialogRect(  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or [CRect](../vs140/CRect-Class.md) object that contains the dialog-box coordinates to be converted.  
  
## Remarks  
 Dialog-box units are stated in terms of the current dialog-box base unit derived from the average width and height of characters in the font used for dialog-box text. One horizontal unit is one-fourth of the dialog-box base-width unit, and one vertical unit is one-eighth of the dialog-box base height unit.  
  
 The **GetDialogBaseUnits** Windows function returns size information for the system font, but you can specify a different font for each dialog box if you use the **DS_SETFONT** style in the resource-definition file. The `MapDialogRect` Windows function uses the appropriate font for this dialog box.  
  
 The `MapDialogRect` member function replaces the dialog-box units in `lpRect` with screen units (pixels) so that the rectangle can be used to create a dialog box or position a control within a box.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [GetDialogBaseUnits](http://msdn.microsoft.com/library/windows/desktop/ms645475)   
 [MapDialogRect](http://msdn.microsoft.com/library/windows/desktop/ms645502)   
 [WM_SETFONT](http://msdn.microsoft.com/library/windows/desktop/ms632642)