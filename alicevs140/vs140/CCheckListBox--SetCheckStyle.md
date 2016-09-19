---
title: "CCheckListBox::SetCheckStyle"
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
ms.assetid: 96c6128e-74cc-45a5-84be-68223f155afe
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCheckListBox::SetCheckStyle
Call this function to set the style of check boxes in the checklist box.  
  
## Syntax  
  
```  
  
      void SetCheckStyle(  
   UINT nStyle   
);  
```  
  
#### Parameters  
 `nStyle`  
 Determines the style of check boxes in the checklist box.  
  
## Remarks  
 Valid styles are:  
  
-   **BS_CHECKBOX**  
  
-   **BS_AUTOCHECKBOX**  
  
-   **BS_AUTO3STATE**  
  
-   **BS_3STATE**  
  
 For information on these styles, see [Button Styles](../vs140/Button-Styles.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCheckListBox Class](../vs140/CCheckListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCheckListBox::SetCheck](../vs140/CCheckListBox--SetCheck.md)   
 [CCheckListBox::GetCheck](../vs140/CCheckListBox--GetCheck.md)   
 [CCheckListBox::GetCheckStyle](../vs140/CCheckListBox--GetCheckStyle.md)