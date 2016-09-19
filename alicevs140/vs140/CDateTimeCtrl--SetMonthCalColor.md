---
title: "CDateTimeCtrl::SetMonthCalColor"
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
ms.assetid: ac7cf434-9ea0-4244-bf03-87a14131c86c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::SetMonthCalColor
Sets the color for a given portion of the month calendar within a date and time picker control.  
  
## Syntax  
  
```  
  
      COLORREF SetMonthCalColor(  
   int iColor,  
   COLORREF ref   
);  
```  
  
#### Parameters  
 `iColor`  
 `int` value specifying which area of the month calendar control to set. This value can be one of the following.  
  
|Value|Meaning|  
|-----------|-------------|  
|MCSC_BACKGROUND|Set the background color displayed between months.|  
|MCSC_MONTHBK|Set the background color displayed within a month.|  
|MCSC_TEXT|Set the color used to display text within a month.|  
|MCSC_TITLEBK|Set the background color displayed in the calendar's title.|  
|MCSC_TITLETEXT|Set the color used to display text within the calendar's title.|  
|MCSC_TRAILINGTEXT|Set the color used to display header and trailing-day text. Header and trailing days are the days from the previous and following months that appear on the current calendar.|  
  
 `ref`  
 A **COLORREF** value representing the color that will be set for the specified area of the month calendar.  
  
## Return Value  
 A **COLORREF** value that represents the previous color setting for the specified portion of the month calendar control if successful. Otherwise, the message returns -1.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [DTM_SETMCCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb761773), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CDateTimeCtrl::GetMonthCalColor](../vs140/CDateTimeCtrl--GetMonthCalColor.md).  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDateTimeCtrl::GetMonthCalColor](../vs140/CDateTimeCtrl--GetMonthCalColor.md)