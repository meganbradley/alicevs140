---
title: "CTaskDialog::NavigateTo"
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
ms.assetid: e3f94035-ec99-44d0-904a-5fed67e6f574
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::NavigateTo
Transfers the focus to another `CTaskDialog`.  
  
## Syntax  
  
```  
protected:  
void NavigateTo(  
   CTaskDialog& oTaskDialog  
) const;  
```  
  
#### Parameters  
 [in] `oTaskDialog`  
 The `CTaskDialog` that receives the focus.  
  
## Remarks  
 This method hides the current `CTaskDialog` when it displays the `oTaskDialog`. The `oTaskDialog` is displayed in the same location as the current `CTaskDialog`.  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)