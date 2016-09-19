---
title: "CCheckListBox::Enable"
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
ms.assetid: 8a78097b-40f4-4cac-a5bf-0067ecda3454
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CCheckListBox::Enable
Call this function to enable or disable a checklist box item.  
  
## Syntax  
  
```  
  
      void Enable(  
   int nIndex,  
   BOOL bEnabled = TRUE   
);  
```  
  
#### Parameters  
 `nIndex`  
 Index of the checklist box item to be enabled.  
  
 `bEnabled`  
 Specifies whether the item is enabled or disabled.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CCheckListBox Class](../vs140/CCheckListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CCheckListBox::IsEnabled](../vs140/CCheckListBox--IsEnabled.md)