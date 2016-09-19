---
title: "CReBarCtrl::MoveBand"
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
ms.assetid: c9c7f084-76d0-40ef-92b7-45d6f79aedc4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::MoveBand
Implements the behavior of the Win32 message [RB_MOVEBAND](http://msdn.microsoft.com/library/windows/desktop/bb774504), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      BOOL MoveBand(  
   UINT uFrom,  
   UINT uTo   
);  
```  
  
#### Parameters  
 *uFrom*  
 Zero-based index of the band to be moved.  
  
 *uTo*  
 Zero-based index of the new band position. This parameter value must never be greater than the number of bands minus one. To obtain the number of bands, call [GetBandCount](../vs140/CReBarCtrl--GetBandCount.md).  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)