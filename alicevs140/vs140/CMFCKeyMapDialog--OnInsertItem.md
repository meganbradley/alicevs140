---
title: "CMFCKeyMapDialog::OnInsertItem"
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
ms.assetid: 4add0fcc-5875-42f2-8253-6ef062e8ba8e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCKeyMapDialog::OnInsertItem
Called by the framework before a new item is inserted into an internal list control that supports the keyboard mapping control.  
  
## Syntax  
  
```  
virtual void OnInsertItem(  
   CMFCToolBarButton* pButton,  
   int nItem   
);  
```  
  
#### Parameters  
 [in] `pButton`  
 A pointer to a toolbar button that is used to map a keyboard key combination to a command name and description. The key map item is stored in an internal list control.  
  
 [in] `nItem`  
 A zero-based index that specifies where to insert the new key map item in the internal list control.  
  
## Remarks  
  
## Requirements  
 **Header:** afxkeymapdialog.h  
  
## See Also  
 [CMFCKeyMapDialog Class](../vs140/CMFCKeyMapDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)