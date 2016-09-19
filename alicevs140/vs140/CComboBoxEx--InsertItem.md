---
title: "CComboBoxEx::InsertItem"
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
ms.assetid: d0fe0057-b2d0-4ba5-aa64-822ab51afaf0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::InsertItem
Inserts a new item in a **ComboBoxEx** control.  
  
## Syntax  
  
```  
  
      int InsertItem(  
   const COMBOBOXEXITEM* pCBItem   
);  
```  
  
#### Parameters  
 `pCBItem`  
 A pointer to a [COMBOBOXEXITEM](http://msdn.microsoft.com/library/windows/desktop/bb775746) structure that will receive the item information. This structure contains callback flag values for the item.  
  
## Return Value  
 The index at which the new item was inserted if successful; otherwise -1.  
  
## Remarks  
 When you call `InsertItem`, a [WM_NOTIFY](http://msdn.microsoft.com/library/windows/desktop/bb775583) message with [CBEN_INSERTITEM](http://msdn.microsoft.com/library/windows/desktop/bb775764) notification will be sent to the parent window.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBoxEx::GetItem](../vs140/CComboBoxEx--GetItem.md)   
 [CComboBoxEx::SetItem](../vs140/CComboBoxEx--SetItem.md)