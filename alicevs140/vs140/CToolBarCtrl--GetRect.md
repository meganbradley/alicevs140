---
title: "CToolBarCtrl::GetRect"
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
ms.assetid: 2f142772-a524-4bf2-9269-0ce3e6e5d356
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::GetRect
Retrieves the bounding rectangle for a specified toolbar button.  
  
## Syntax  
  
```  
  
      BOOL GetRect(  
   int nID,  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `nID`  
 The button identifier.  
  
 `lpRect`  
 A pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure to receive the bounding rectangle information.  
  
## Return Value  
 **TRUE** if successful; otherwise **FALSE**.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [TB_GETRECT](http://msdn.microsoft.com/library/windows/desktop/bb787346), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)