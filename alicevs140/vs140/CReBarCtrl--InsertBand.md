---
title: "CReBarCtrl::InsertBand"
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
ms.assetid: d07b5831-fe54-4235-9f7c-d3a887411f3b
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::InsertBand
Implements the behavior of the Win32 message [RB_INSERTBAND](http://msdn.microsoft.com/library/windows/desktop/bb774498), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL InsertBand(  
   UINT uIndex,  
   REBARBANDINFO* prbbi   
);  
```  
  
#### Parameters  
 *uIndex*  
 Zero-based index of the location where the band will be inserted. If you set this parameter to -1, the control will add the new band at the last location.  
  
 `prbbi`  
 A pointer to a [REBARBANDINFO](http://msdn.microsoft.com/library/windows/desktop/bb774393) structure that defines the band to be inserted. You must set the `cbSize` member of this structure to `sizeof(REBARBANDINFO)` before calling this function.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#9](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#9)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)