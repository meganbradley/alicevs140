---
title: "CMonthCalCtrl::SetRange"
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
ms.assetid: f29ffd13-2862-4386-a3f2-0edd865c7029
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetRange
Sets the minimum and maximum allowable dates for a month calendar control.  
  
## Syntax  
  
```  
  
      BOOL SetRange(  
   const COleDateTime* pMinRange,  
   const COleDateTime* pMaxRange   
);  
BOOL SetRange(  
   const CTime* pMinRange,  
   const CTime* pMaxRange   
);  
BOOL SetRange(  
   const LPSYSTEMTIME pMinRange,  
   const LPSYSTEMTIME pMaxRange   
);  
```  
  
#### Parameters  
 `pMinRange`  
 A pointer to a `COleDateTime` object, a `CTime` object, or [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure containing the date at the lowest end of the range.  
  
 `pMaxRange`  
 A pointer to a `COleDateTime` object, a `CTime` object, or `SYSTEMTIME` structure containing the date at the highest end of the range.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_SETRANGE](http://msdn.microsoft.com/library/windows/desktop/bb761012), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. In MFC's implementation of `SetRange`, you can specify `COleDateTime` usage, a `CTime` usage, or a `SYSTEMTIME` structure usage.  
  
## Example  
 See the example for [CMonthCalCtrl::GetRange](../vs140/CMonthCalCtrl--GetRange.md).  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::GetRange](../vs140/CMonthCalCtrl--GetRange.md)