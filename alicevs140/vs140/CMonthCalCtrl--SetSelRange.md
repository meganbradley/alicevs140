---
title: "CMonthCalCtrl::SetSelRange"
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
ms.assetid: 1e398c9e-53b1-45be-be4c-e125cc978dc9
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetSelRange
Sets the selection for a month calendar control to a given date range.  
  
## Syntax  
  
```  
  
      BOOL SetSelRange(  
   const COleDateTime& pMinRange,  
   const COleDateTime& pMaxRange   
);  
BOOL SetSelRange(  
   const CTime& pMinRange,  
   const CTime& pMaxRange   
);  
BOOL SetSelRange(  
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
 This member function implements the behavior of the Win32 message [MCM_SETSELRANGE](http://msdn.microsoft.com/library/windows/desktop/bb761014), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. In MFC's implementation of `SetSelRange`, you can specify `COleDateTime` usage, a `CTime` usage, or a `SYSTEMTIME` structure usage.  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::GetSelRange](../vs140/CMonthCalCtrl--GetSelRange.md)