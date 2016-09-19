---
title: "CComboBoxEx::GetComboBoxCtrl"
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
ms.assetid: a992345c-c9cb-404e-8948-d82c85d65e2e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBoxEx::GetComboBoxCtrl
Call this member function to get a pointer to a combo box control within a `CComboBoxEx` object.  
  
## Syntax  
  
```  
  
CComboBox* GetComboBoxCtrl( );  
  
```  
  
## Return Value  
 A pointer to a `CComboBox` object.  
  
## Remarks  
 The `CComboBoxEx` control consists of a parent window, which encapsulates a `CComboBox`.  
  
 The `CComboBox` object pointed to by the return value is a temporary object and is destroyed during the next idle processing time.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CComboBoxEx Class](../vs140/CComboBoxEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBoxEx::GetEditCtrl](../vs140/CComboBoxEx--GetEditCtrl.md)