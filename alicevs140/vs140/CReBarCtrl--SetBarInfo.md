---
title: "CReBarCtrl::SetBarInfo"
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
ms.assetid: bd4e0eab-1d73-4e67-b27b-21b524b3673c
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetBarInfo
Implements the behavior of the Win32 message [RB_SETBARINFO](http://msdn.microsoft.com/library/windows/desktop/bb774513), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL SetBarInfo(  
   REBARINFO* prbi   
);  
```  
  
#### Parameters  
 `prbi`  
 A pointer to a [REBARINFO](http://msdn.microsoft.com/library/windows/desktop/bb774395) structure that contains the information to be set. You must set the `cbSize` member of this structure to `sizeof(REBARINFO)` before sending this message  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#14)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::GetBarInfo](../vs140/CReBarCtrl--GetBarInfo.md)