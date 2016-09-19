---
title: "CTaskDialog::IsSupported"
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
ms.assetid: e6b7e62a-87ba-44e9-aa04-39746e1a4b5b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::IsSupported
Determines whether the computer that is running the application supports the `CTaskDialog`.  
  
## Syntax  
  
```  
static BOOL IsSupported();  
```  
  
## Return Value  
 `TRUE` if the computer supports the `CTaskDialog`; `FALSE` otherwise.  
  
## Remarks  
 Use this function to determine at runtime if the computer that is running your application supports the [CTaskDialog Class](../vs140/CTaskDialog-Class.md). If the computer does not support the `CTaskDialog`, you should provide another method of communicating information to the user. Your application will crash if it tries to use a `CTaskDialog` on a computer that does not support the `CTaskDialog` class.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#1](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#1)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)