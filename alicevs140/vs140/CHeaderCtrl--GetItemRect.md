---
title: "CHeaderCtrl::GetItemRect"
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
ms.assetid: 0ce628ab-7fd5-45c0-9121-6bcc78d3c232
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::GetItemRect
Retrieves the bounding rectangle for a given item in a header control.  
  
## Syntax  
  
```  
  
      BOOL GetItemRect(  
   int nIndex,  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 The zero-based index of the header control item.  
  
 `lpRect`  
 A pointer to the address of a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that receives the bounding rectangle information.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This method implements the behavior of the Win32 message [HDM_GETITEMRECT](http://msdn.microsoft.com/library/windows/desktop/bb775341), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)