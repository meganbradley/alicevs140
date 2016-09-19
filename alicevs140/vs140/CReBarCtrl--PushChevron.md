---
title: "CReBarCtrl::PushChevron"
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
ms.assetid: f2f65a65-604f-4cca-a999-71df50fae2ac
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::PushChevron
Implements the behavior of the Win32 message [RB_PUSHCHEVRON](http://msdn.microsoft.com/library/windows/desktop/bb774506), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Syntax  
  
```  
  
      void PushChevron(  
   UINT uBand,  
   LPARAM lAppValue   
);  
```  
  
#### Parameters  
 `uBand`  
 Zero-based index of the band whose chevron is to be pushed.  
  
 `lAppValue`  
 An application defined 32-bit value. See `lAppValue` in [RB_PUSHCHEVRON](http://msdn.microsoft.com/library/windows/desktop/bb774506) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)