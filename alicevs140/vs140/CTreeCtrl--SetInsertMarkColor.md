---
title: "CTreeCtrl::SetInsertMarkColor"
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
ms.assetid: 9d3272ff-0ad4-46ac-bb7a-93facd279c15
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTreeCtrl::SetInsertMarkColor
This member function implements the behavior of the Win32 message [TVM_SETINSERTMARKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb773755), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      COLORREF SetInsertMarkColor(  
   COLORREF clrNew   
);  
```  
  
#### Parameters  
 `clrNew`  
 A **COLORREF** value that contains the new insertion mark color.  
  
## Return Value  
 A **COLORREF** value that contains the previous insertion mark color.  
  
## Example  
 See the example for [CTreeCtrl::GetInsertMarkColor](../vs140/CTreeCtrl--GetInsertMarkColor.md).  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CTreeCtrl Class](../vs140/CTreeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTreeCtrl::GetInsertMarkColor](../vs140/CTreeCtrl--GetInsertMarkColor.md)