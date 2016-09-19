---
title: "CComboBoxEx::GetEditCtrl"
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
ms.assetid: 2306afa0-26b7-4a44-a8f7-7f87616e2a17
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::GetEditCtrl
Call this member function to get a pointer to the edit control for a combo box.  
  
## Syntax  
  
```  
  
CEdit* GetEditCtrl( );  
  
```  
  
## Return Value  
 A pointer to a [CEdit](../vs140/CEdit-Class.md) object.  
  
## Remarks  
 A `CComboBoxEx` control uses an edit box when it is created with the **CBS_DROPDOWN** style.  
  
 The `CEdit` object pointed to by the return value is a temporary object and is destroyed during the next idle processing time.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBoxEx::Create](../vs140/CComboBoxEx--Create.md)   
 [CComboBoxEx::CreateEx](../vs140/CComboBoxEx--CreateEx.md)