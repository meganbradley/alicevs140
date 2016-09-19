---
title: "CMonthCalCtrl::GetToday"
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
ms.assetid: 681f42e9-11f5-4bdd-a788-b0e656bc52d7
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetToday
Retrieves the date information for the date specified as "today" for a month calendar control.  
  
## Syntax  
  
```  
  
      BOOL GetToday(   
   COleDateTime& refDateTime    
) const;  
BOOL GetToday(   
   COleDateTime& refDateTime    
) const;  
BOOL GetToday(  
   LPSYSTEMTIME pDateTime   
) const;  
```  
  
#### Parameters  
 `refDateTime`  
 A reference to a [COleDateTime](../vs140/COleDateTime-Class.md) or [CTime](../Topic/CTime%20Class.md) object indicating the current day.  
  
 `pDateTime`  
 A pointer to a [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure that will receive the date information. This parameter must be a valid address and cannot be **NULL**.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [MCM_GETTODAY](http://msdn.microsoft.com/library/windows/desktop/bb760987), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. In MFC's implementation of `GetToday`, you can specify a `COleDateTime` usage, a `CTime` usage, or a `SYSTEMTIME` structure usage.  
  
## Example  
 [!CODE [NVC_MFC_CMonthCalCtrl#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CMonthCalCtrl#3)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMonthCalCtrl::SetToday](../vs140/CMonthCalCtrl--SetToday.md)