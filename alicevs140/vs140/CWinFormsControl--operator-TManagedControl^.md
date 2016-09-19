---
title: "CWinFormsControl::operator TManagedControl^"
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
ms.assetid: 5256564b-7ba8-43b4-95c8-6b199be75ac2
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWinFormsControl::operator TManagedControl^
Casts a type as a pointer to a Windows Forms control.  
  
## Syntax  
  
```  
inline operator TManagedControl^( ) const;  
```  
  
## Remarks  
 This operator passes `CWinFormsControl<``TManagedControl``>` to functions that accept a pointer to a Windows Forms control.  
  
## Requirements  
 **Header:** afxwinforms.h  
  
## See Also  
 [CWinFormsControl Class](../vs140/CWinFormsControl-Class.md)