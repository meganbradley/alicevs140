---
title: "CMFCToolBarDateTimeCtrl::GetTimeAll"
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
ms.assetid: 59d13f47-ef55-48dd-9862-551548abd439
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::GetTimeAll
Returns the time selected by the user from the time picker control button that has a specified command ID.  
  
## Syntax  
  
```  
static BOOL GetTimeAll(  
   UINT uiCmd,  
   COleDateTime& timeDest   
);  
static DWORD GetTimeAll(  
   UINT uiCmd,  
   CTime& timeDest   
);  
static DWORD GetTimeAll(  
   UINT uiCmd,  
   LPSYSTEMTIME pTimeDest   
);  
```  
  
#### Parameters  
 `[in] uiCmd`  
 Specifies a toolbar button's command ID.  
  
 `[out] timeDest`  
 In the first overload, a [COleDateTime](../vs140/COleDateTime-Class.md) object that will receive the system time information. In the second overload, a [CTime](../Topic/CTime%20Class.md) object that will receive the system time information.  
  
 `[out] pTimeDest`  
 A pointer to the [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure to receive the system time information. Must not be `NULL`.  
  
## Return Value  
 If the framework cannot find a toolbar button that matches the command ID `uiCmd`, the return value is zero in the first overload, and GDT_NONE in the other overloads. If the toolbar button is found, the return value is the same as the return value from a call to [CMFCToolBarDateTimeCtrl::GetTime](../vs140/CMFCToolBarDateTimeCtrl--GetTime.md) on that button. A return value of zero or GDT_NONE can occur when the button is found, which indicates that the call to `GetTime` did not return a valid date for some other reason.  
  
## Remarks  
 This method looks for a toolbar button that has the specified command ID and calls [CMFCToolBarDateTimeCtrl::GetTime](../vs140/CMFCToolBarDateTimeCtrl--GetTime.md) method on that button.  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)