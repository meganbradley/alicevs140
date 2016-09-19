---
title: "CMonthCalCtrl::SetDayState"
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
ms.assetid: 74de8d66-1edf-4c44-ac4e-9bb93ca4668a
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SetDayState
Sets the display for days in a month calendar control.  
  
## Syntax  
  
```  
  
      BOOL SetDayState(  
   int nMonths,  
   LPMONTHDAYSTATE pStates   
);  
```  
  
#### Parameters  
 *nMonths*  
 Value indicating how many elements are in the array that `pStates` points to.  
  
 `pStates`  
 A pointer to a [MONTHDAYSTATE](http://msdn.microsoft.com/library/windows/desktop/bb760915) array of values that define how the month calendar control will draw each day in its display. The **MONTHDAYSTATE** data type is a bit field, where each bit (1 through 31) represents the state of a day in a month. If a bit is on, the corresponding day will be displayed in bold; otherwise it will be displayed with no emphasis.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_SETDAYSTATE](http://msdn.microsoft.com/library/windows/desktop/bb761004), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CMonthCalCtrl#6](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl#6)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)