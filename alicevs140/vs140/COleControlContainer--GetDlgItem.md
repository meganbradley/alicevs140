---
title: "COleControlContainer::GetDlgItem"
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
ms.assetid: 0a0846d4-bfbf-4a38-9adc-a7a171ce2a4e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControlContainer::GetDlgItem
Retrieves a pointer to the specified control or child window in a dialog box or other window.  
  
## Syntax  
  
```  
  
      virtual CWnd* GetDlgItem(  
   int nID   
) const;  
virtual void GetDlgItem(  
   int nID,  
   HWND* phWnd   
) const;  
```  
  
#### Parameters  
 `nID`  
 Identifier of the dialog item to retrieve.  
  
 `phWnd`  
 A pointer to the handle of the specified dialog item's window object.  
  
## Return Value  
 A pointer to the dialog item's window.  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COleControlContainer Class](../vs140/COleControlContainer-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)