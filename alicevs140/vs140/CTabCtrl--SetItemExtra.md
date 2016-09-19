---
title: "CTabCtrl::SetItemExtra"
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
ms.assetid: 483661ab-ff82-4e9f-974a-1712fac93d5e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTabCtrl::SetItemExtra
Sets the number of bytes per tab reserved for application-defined data in a tab control.  
  
## Syntax  
  
```  
  
      BOOL SetItemExtra(  
  int nBytes   
);  
```  
  
#### Parameters  
 `nBytes`  
 The number of extra bytes to set.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TCM_SETITEMEXTRA](http://msdn.microsoft.com/library/windows/desktop/bb760633), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTabCtrl Class](../vs140/CTabCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTabCtrl::SetItem](../vs140/CTabCtrl--SetItem.md)