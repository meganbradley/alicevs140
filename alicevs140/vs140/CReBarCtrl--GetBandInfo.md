---
title: "CReBarCtrl::GetBandInfo"
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
ms.assetid: d51a9c07-24b3-4719-a6c0-f32400b3c79d
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetBandInfo
Implements the behavior of the Win32 message [RB_GETBANDINFO](http://msdn.microsoft.com/library/windows/desktop/bb774451) as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL GetBandInfo(  
   UINT uBand,  
   REBARBANDINFO* prbbi   
) const;  
```  
  
#### Parameters  
 `uBand`  
 Zero-based index of the band for which the information will be retrieved.  
  
 `prbbi`  
 A pointer to a [REBARBANDINFO](http://msdn.microsoft.com/library/windows/desktop/bb774393) structure to receive the band information. You must set the `cbSize` member of this structure to `sizeof(REBARBANDINFO)` and set the **fMask** member to the items you want to retrieve before sending this message.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::SetBandInfo](../vs140/CReBarCtrl--SetBandInfo.md)   
 [CReBarCtrl::GetBandCount](../vs140/CReBarCtrl--GetBandCount.md)   
 [CReBarCtrl::DeleteBand](../vs140/CReBarCtrl--DeleteBand.md)   
 [CReBarCtrl::InsertBand](../vs140/CReBarCtrl--InsertBand.md)   
 [CReBarCtrl::ShowBand](../vs140/CReBarCtrl--ShowBand.md)