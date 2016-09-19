---
title: "CMonthCalCtrl::GetCurSel"
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
ms.assetid: 2d1b1530-3919-45c1-a904-87a978b69dd5
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetCurSel
Retrieves the system time as indicated by the currently-selected date.  
  
## Syntax  
  
```  
  
      BOOL GetCurSel(  
   COleDateTime& refDateTime   
) const;  
BOOL GetCurSel(  
   CTime& refDateTime   
) const;  
BOOL GetCurSel(  
   LPSYSTEMTIME pDateTime   
) const;  
```  
  
#### Parameters  
 `refDateTime`  
 A reference to a [COleDateTime](../vs140/COleDateTime-Class.md) object or a [CTime](../Topic/CTime%20Class.md) object. Receives the current time.  
  
 `pDateTime`  
 A pointer to a [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure that will receive the currently-selected date information. This parameter must be a valid address and cannot be **NULL**.  
  
## Return Value  
 Nonzero if successful; otherwize 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_GETCURSEL](http://msdn.microsoft.com/library/windows/desktop/bb760957), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
> [!NOTE]
>  This member function fails if the style **MCS_MULTISELECT** is set.  
  
 In MFC's implementation of `GetCurSel`, you can specify a `COleDateTime` usage, a `CTime` usage, or a `SYSTEMTIME` structure usage.  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::SetCurSel](../vs140/CMonthCalCtrl--SetCurSel.md)