---
title: "CMFCPopupMenu::InsertSeparator"
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
ms.assetid: c70c95bb-e7be-45c5-a7f1-096fdb1cd47c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCPopupMenu::InsertSeparator
Inserts a separator into the pop-up menu at the specified location.  
  
## Syntax  
  
```  
int InsertSeparator(  
   int iInsertAt = -1  
);  
```  
  
#### Parameters  
 [in] `iInsertAt`  
 The zero-based index of the position where this method will insert the separator.  
  
## Return Value  
 The zero-based index of the position where the separator was inserted. -1 if this method fails.  
  
## Remarks  
 A value of -1 for `iInsertAt` means this method will add the separator to the end of the pop-up menu.  
  
 This method fails if `iInsertAt` is an invalid value.  
  
## Requirements  
 **Header:** afxpopupmenu.h  
  
## See Also  
 [CMFCPopupMenu Class](../vs140/CMFCPopupMenu-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)