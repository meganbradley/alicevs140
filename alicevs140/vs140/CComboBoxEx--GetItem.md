---
title: "CComboBoxEx::GetItem"
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
ms.assetid: f2daa854-6962-4ac8-824d-92f8fdcf8232
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::GetItem
Retrieves item information for a given **ComboBoxEx** item.  
  
## Syntax  
  
```  
  
      BOOL GetItem(  
   COMBOBOXEXITEM* pCBItem   
);  
```  
  
#### Parameters  
 `pCBItem`  
 A pointer to a [COMBOBOXEXITEM](http://msdn.microsoft.com/library/windows/desktop/bb775746) structure that will receive the item information.  
  
## Return Value  
 Nonzero if the operation was successful; otherwise 0.  
  
## Remarks  
 This member function implements the functionality of the message [CBEM_GETITEM](http://msdn.microsoft.com/library/windows/desktop/bb775779), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBoxEx::SetItem](../vs140/CComboBoxEx--SetItem.md)   
 [CComboBoxEx::InsertItem](../vs140/CComboBoxEx--InsertItem.md)