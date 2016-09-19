---
title: "CMonthCalCtrl::GetMinReqRect"
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
ms.assetid: d3818ee9-d529-4ad1-ad47-29df02f390ac
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetMinReqRect
Retrieves the minimum size required to show a full month in a month calendar control.  
  
## Syntax  
  
```  
  
      BOOL GetMinReqRect(  
   RECT* pRect   
) const;  
```  
  
#### Parameters  
 `pRect`  
 A pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that will receive bounding rectangle information. This parameter must be a valid address and cannot be **NULL**.  
  
## Return Value  
 If successful, this member function returns nonzero and `lpRect` receives the applicable bounding information. If unsuccessful, the member function returns 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_GETMINREQRECT](http://msdn.microsoft.com/library/windows/desktop/bb760978), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::SizeMinReq](../vs140/CMonthCalCtrl--SizeMinReq.md)