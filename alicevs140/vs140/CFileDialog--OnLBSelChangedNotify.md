---
title: "CFileDialog::OnLBSelChangedNotify"
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
ms.assetid: 9fe672a7-f61c-4fe9-978f-0547489ff266
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::OnLBSelChangedNotify
This function is called whenever the current selection in a list box is about to change.  
  
## Syntax  
  
```  
  
      virtual void OnLBSelChangedNotify(  
   UINT nIDBox,  
   UINT iCurSel,  
   UINT nCode  
);  
```  
  
#### Parameters  
 *nIDBox*  
 The ID of the list box or combo box in which the selection occurred.  
  
 `iCurSel`  
 The index of the current selection.  
  
 `nCode`  
 The control notification code. This parameter must have one of the following values:  
  
-   **CD_LBSELCHANGE** Specifies `iCurSel` is the selected item in a single-selection list box.  
  
-   **CD_LBSELSUB** Specifies that `iCurSel` is no longer selected in a multiselection list box.  
  
-   **CD_LBSELADD** Specifies that `iCurSel` is selected in a multiselection list box.  
  
-   **CD_LBSELNOITEMS** Specifies that no selection exists in a multiselection list box.  
  
## Remarks  
 Override this function to provide custom handling of selection changes in the list box. For example, you can use this function to display the access rights or date-last-modified of each file the user selects.  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)