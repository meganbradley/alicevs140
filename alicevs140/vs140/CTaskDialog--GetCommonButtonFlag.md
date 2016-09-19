---
title: "CTaskDialog::GetCommonButtonFlag"
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
ms.assetid: 4384bd62-ef83-46bb-94cd-7f3d4efadde3
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::GetCommonButtonFlag
Converts a standard Windows button to the common button type associated with the [CTaskDialog Class](../vs140/CTaskDialog-Class.md).  
  
## Syntax  
  
```  
int GetCommonButtonFlag(  
   int nButtonId  
) const;  
```  
  
#### Parameters  
 [in] `nButtonId`  
 The standard Windows button value.  
  
## Return Value  
 The value of the corresponding `CTaskDialog` common button. If there is no corresponding common button, this method returns 0.  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::GetCommonButtonId](../vs140/CTaskDialog--GetCommonButtonId.md)   
 [CTaskDialog::GetCommonButtonCount](../vs140/CTaskDialog--GetCommonButtonCount.md)