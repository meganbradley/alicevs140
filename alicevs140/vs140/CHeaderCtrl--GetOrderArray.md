---
title: "CHeaderCtrl::GetOrderArray"
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
ms.assetid: 73aa7231-9e46-47c5-86de-ee3421419dfb
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHeaderCtrl::GetOrderArray
Retrieves the left-to-right order of items in a header control.  
  
## Syntax  
  
```  
  
      BOOL GetOrderArray(  
   LPINT piArray,  
   int iCount  
);  
```  
  
#### Parameters  
 `piArray`  
 A pointer to the address of a buffer that receives the index values of the items in the header control, in the order in which they appear from left to right.  
  
 `iCount`  
 The number of header control items. Must be non-negative.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [HDM_GETORDERARRAY](http://msdn.microsoft.com/library/windows/desktop/bb775343), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. It is provided to support header item ordering.  
  
## Example  
 [!CODE [NVC_MFC_CHeaderCtrl#11](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CHeaderCtrl#11)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CHeaderCtrl Class](../vs140/CHeaderCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHeaderCtrl::SetOrderArray](../vs140/CHeaderCtrl--SetOrderArray.md)   
 [CHeaderCtrl::OrderToIndex](../vs140/CHeaderCtrl--OrderToIndex.md)