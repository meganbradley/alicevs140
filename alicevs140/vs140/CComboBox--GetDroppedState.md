---
title: "CComboBox::GetDroppedState"
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
ms.assetid: 90b75de4-104a-46e1-aa26-3e75ec7a8095
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetDroppedState
Call the `GetDroppedState` member function to determine whether the list box of a drop-down combo box is visible (dropped down).  
  
## Syntax  
  
```  
  
BOOL GetDroppedState( ) const;  
```  
  
## Return Value  
 Nonzero if the list box is visible; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CComboBox#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CComboBox#17)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CB_SHOWDROPDOWN](http://msdn.microsoft.com/library/windows/desktop/bb775919)   
 [CB_GETDROPPEDSTATE](http://msdn.microsoft.com/library/windows/desktop/bb775849)