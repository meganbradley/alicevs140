---
title: "CReBarCtrl::IDToIndex"
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
ms.assetid: 454c676b-19fe-46c4-a5c9-516927b9152f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::IDToIndex
Implements the behavior of the Win32 message [RB_IDTOINDEX](http://msdn.microsoft.com/library/windows/desktop/bb774496), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      int IDToIndex(  
   UINT uBandID   
) const;  
```  
  
#### Parameters  
 *uBandID*  
 The application-defined identifier of the specified band, passed in the **wID** member of the [REBARBANDINFO](http://msdn.microsoft.com/library/windows/desktop/bb774393) structure when the band is inserted.  
  
## Return Value  
 The zero-based band index if successful, or -1 otherwise. If duplicate band indices exist, the first one is returned.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CReBarCtrl::InsertBand](../vs140/CReBarCtrl--InsertBand.md)