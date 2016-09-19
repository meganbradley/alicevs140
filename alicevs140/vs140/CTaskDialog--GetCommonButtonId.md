---
title: "CTaskDialog::GetCommonButtonId"
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
ms.assetid: 842c5903-f0c7-4130-9e27-54917dca2a23
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::GetCommonButtonId
Converts one of the common button types associated with the [CTaskDialog Class](../vs140/CTaskDialog-Class.md) to a standard Windows button.  
  
## Syntax  
  
```  
int GetCommonButtonId(  
   int nFlag  
);  
```  
  
#### Parameters  
 [in] `nFlag`  
 The common button type associated with the `CTaskDialog` class.  
  
## Return Value  
 The value of the corresponding standard Windows button. If there is no corresponding Windows button, the method returns 0.  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::GetCommonButtonFlag](../vs140/CTaskDialog--GetCommonButtonFlag.md)   
 [CTaskDialog::GetCommonButtonCount](../vs140/CTaskDialog--GetCommonButtonCount.md)