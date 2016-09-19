---
title: "COleControlContainer::CheckDlgButton"
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
ms.assetid: 0fcc7425-01df-4d5b-9577-f2c57bc55d95
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::CheckDlgButton
Modifies the current state of the button.  
  
## Syntax  
  
```  
  
      virtual void CheckDlgButton(  
   int nIDButton,  
   UINT nCheck   
);  
```  
  
#### Parameters  
 `nIDButton`  
 The ID of the button to be modified.  
  
 `nCheck`  
 Specifies the state of the button. Can be one of the following:  
  
-   **BST_CHECKED** Sets the button state to checked.  
  
-   **BST_INDETERMINATE** Sets the button state to grayed, indicating an indeterminate state. Use this value only if the button has the **BS_3STATE** or **BS_AUTO3STATE** style.  
  
-   **BST_UNCHECKED** Sets the button state to cleared.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)