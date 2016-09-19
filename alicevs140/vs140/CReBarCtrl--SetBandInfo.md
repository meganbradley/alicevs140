---
title: "CReBarCtrl::SetBandInfo"
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
ms.assetid: d6b0d2c7-c1e9-4901-ae80-67bcc9d0c2f9
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::SetBandInfo
Implements the behavior of the Win32 message [RB_SETBANDINFO](http://msdn.microsoft.com/library/windows/desktop/bb774508), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL SetBandInfo(  
   UINT uBand,  
   REBARBANDINFO* prbbi   
);  
```  
  
#### Parameters  
 `uBand`  
 Zero-based index of the band to receive the new settings.  
  
 `prbbi`  
 Pointer to a [REBARBANDINFO](http://msdn.microsoft.com/library/windows/desktop/bb774393) structure that defines the band to be inserted. You must set the `cbSize` member of this structure to `sizeof(REBARBANDINFO)` before sending this message.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#13](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#13)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::GetBandInfo](../vs140/CReBarCtrl--GetBandInfo.md)