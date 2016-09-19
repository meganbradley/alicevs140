---
title: "CComboBoxEx::SetItem"
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
ms.assetid: d979b83c-29e0-4d1f-afe8-39540f9ae12e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::SetItem
Sets the attributes for an item in a **ComboBoxEx** control.  
  
## Syntax  
  
```  
  
      BOOL SetItem(  
   const COMBOBOXEXITEM* pCBItem   
);  
```  
  
#### Parameters  
 `pCBItem`  
 A pointer to a [COMBOBOXEXITEM](http://msdn.microsoft.com/library/windows/desktop/bb775746) structure that will receive the item information.  
  
## Return Value  
 Nonzero if the operation was successful; otherwise 0.  
  
## Remarks  
 This member function implements the functionality of the message [CBEM_SETITEM](http://msdn.microsoft.com/library/windows/desktop/bb775788), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBoxEx::GetItem](../vs140/CComboBoxEx--GetItem.md)   
 [CComboBoxEx::InsertItem](../vs140/CComboBoxEx--InsertItem.md)