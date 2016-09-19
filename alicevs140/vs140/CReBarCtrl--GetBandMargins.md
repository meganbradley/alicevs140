---
title: "CReBarCtrl::GetBandMargins"
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
ms.assetid: f789d84c-aa0a-4a1c-bf62-f7e370609d3b
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBarCtrl::GetBandMargins
Retrieves the margins of the band.  
  
## Syntax  
  
```  
  
      void GetBandMargins(   
   PMARGINS pMargins   
);  
```  
  
#### Parameters  
 *pMargins*  
 A pointer to a [MARGINS](http://msdn.microsoft.com/library/windows/desktop/bb773244)structure that will receive the information.  
  
## Remarks  
 This member function emulates the functionality of the [RB_GETBANDMARGINS](http://msdn.microsoft.com/library/windows/desktop/bb774453) message, as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CReBarCtrl Class](../vs140/CReBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)