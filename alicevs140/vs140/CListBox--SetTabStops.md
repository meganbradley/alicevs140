---
title: "CListBox::SetTabStops"
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
ms.assetid: 68d0e66c-ca54-460f-a8d3-521a2d7fb6a5
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetTabStops
Sets the tab-stop positions in a list box.  
  
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
 Tab stops are set at every `cxEachStop` dialog units. See *rgTabStops* for a description of a dialog unit.  
  
 `nTabStops`  
 Specifies the number of tab stops to have in the list box.  
  
 `rgTabStops`  
 Points to the first member of an array of integers containing the tab-stop positions in dialog units. A dialog unit is a horizontal or vertical distance. One horizontal dialog unit is equal to one-fourth of the current dialog base width unit, and one vertical dialog unit is equal to one-eighth of the current dialog base height unit. The dialog base units are computed based on the height and width of the current system font. The **GetDialogBaseUnits** Windows function returns the current dialog base units in pixels. The tab stops must be sorted in increasing order; back tabs are not allowed.  
  
## Return Value  
 Nonzero if all the tabs were set; otherwise 0.  
  
## Remarks  
 To set tab stops to the default size of 2 dialog units, call the parameterless version of this member function. To set tab stops to a size other than 2, call the version with the `cxEachStop` argument.  
  
 To set tab stops to an array of sizes, use the version with the `rgTabStops` and `nTabStops` arguments. A tab stop will be set for each value in `rgTabStops`, up to the number specified by `nTabStops`.  
  
 To respond to a call to the `SetTabStops` member function, the list box must have been created with the [LBS_USETABSTOPS](../vs140/List-Box-Styles.md) style.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#39](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#39)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [LB_SETTABSTOPS](http://msdn.microsoft.com/library/windows/desktop/bb761354)   
 [GetDialogBaseUnits](http://msdn.microsoft.com/library/windows/desktop/ms645475)