---
title: "CMonthCalCtrl::GetMonthRange"
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
ms.assetid: 3ef66af0-5c21-4665-888d-ec9494190097
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetMonthRange
Retrieves date information representing the high and low limits of a month calendar control's display.  
  
## Syntax  
  
```  
  
      int GetMonthRange(  
   COleDateTime& refMinRange,  
   COleDateTime& refMaxRange,  
   DWORD dwFlags   
) const;  
int GetMonthRange(  
   CTime& refMinRange,  
   CTime& refMaxRange,  
   DWORD dwFlags   
) const;  
int GetMonthRange(  
   LPSYSTEMTIME pMinRange,  
   LPSYSTEMTIME pMaxRange,  
   DWORD dwFlags   
) const;  
```  
  
#### Parameters  
 `refMinRange`  
 A reference to a [COleDateTime](../vs140/COleDateTime-Class.md) or [CTime](../Topic/CTime%20Class.md) object containing the minimum date allowed.  
  
 `refMaxRange`  
 A reference to a `COleDateTime` or `CTime` object containing the maximum date allowed.  
  
 `pMinRange`  
 A pointer to a [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure containing the date at the lowest end of the range.  
  
 `pMaxRange`  
 A pointer to a `SYSTEMTIME` structure containing the date at the highest end of the range.  
  
 `dwFlags`  
 Value specifying the scope of the range limits to be retrieved. This value must be one of the following.  
  
|Value|Meaning|  
|-----------|-------------|  
|GMR_DAYSTATE|Include preceding and trailing months of visible range that are only partially displayed.|  
|GMR_VISIBLE|Include only those months that are entirely displayed.|  
  
## Return Value  
 An integer that represents the range, in months, spanned by the two limits indicated by `refMinRange` and `refMaxRange` in the first and second versions, or `pMinRange` and `pMaxRange` in the third version.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_GETMONTHRANGE](http://msdn.microsoft.com/library/windows/desktop/bb760981), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. In MFC's implementation of `GetMonthRange`, you can specify `COleDateTime` usage, a `CTime` usage, or a `SYSTEMTIME` structure usage.  
  
## Example  
 See the example for [CMonthCalCtrl::SetDayState](../vs140/CMonthCalCtrl--SetDayState.md).  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::GetRange](../vs140/CMonthCalCtrl--GetRange.md)