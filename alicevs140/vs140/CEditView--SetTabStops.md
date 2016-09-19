---
title: "CEditView::SetTabStops"
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
ms.assetid: d29d34d9-7cb4-4fc7-8747-e5c183fa9f20
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::SetTabStops
Call this function to set the tab stops used for display and printing.  
  
## Syntax  
  
```  
  
      void SetTabStops(  
   int nTabStops   
);  
```  
  
#### Parameters  
 `nTabStops`  
 Width of each tab stop, in dialog units.  
  
## Remarks  
 Only a single tab-stop width is supported. (`CEdit` objects support multiple tab widths.) Widths are in dialog units, which equal one-fourth of the average character width (based on uppercase and lowercase alphabetic characters only) of the font used at the time of printing or displaying. You should not use `CEdit::SetTabStops` because `CEditView` must cache the tab-stop value.  
  
 This function modifies only the tabs of the object for which it is called. To change the tab stops for each `CEditView` object in your application, call each object's `SetTabStops` function.  
  
## Example  
 This code fragment sets the tab stops in the control to every fourth character by carefully measuring the font the control uses.  
  
 [!CODE [NVC_MFCDocView#67](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#67)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::SetFont](../vs140/CWnd--SetFont.md)   
 [CEditView::SetPrinterFont](../vs140/CEditView--SetPrinterFont.md)