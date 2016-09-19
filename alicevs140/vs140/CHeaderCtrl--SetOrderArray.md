---
title: "CHeaderCtrl::SetOrderArray"
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
ms.assetid: c42827e1-0f99-437d-9998-317cc54b8d9f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::SetOrderArray
Sets the left-to-right order of items in a header control.  
  
## Syntax  
  
```  
  
      BOOL SetOrderArray(  
   int iCount,  
   LPINT piArray   
);  
```  
  
#### Parameters  
 `iCount`  
 The number of header control items.  
  
 `piArray`  
 A pointer to the address of a buffer that receives the index values of the items in the header control, in the order in which they appear from left to right.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 macro [HDM_SETORDERARRAY](http://msdn.microsoft.com/library/windows/desktop/bb775369), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. It is provided to support header item ordering.  
  
## Example  
 See the example for [CHeaderCtrl::GetOrderArray](../vs140/CHeaderCtrl--GetOrderArray.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::GetOrderArray](../vs140/CHeaderCtrl--GetOrderArray.md)   
 [CHeaderCtrl::OrderToIndex](../vs140/CHeaderCtrl--OrderToIndex.md)