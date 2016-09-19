---
title: "CDateTimeCtrl::GetTime"
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
ms.assetid: dac2f585-bd6a-4908-8556-8d7088efe4b2
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::GetTime
Retrieves the currently selected time from a date and time picker control and puts it in a specified `SYSTEMTIME` structure.  
  
## Syntax  
  
```  
  
      BOOL GetTime(  
   COleDateTime& timeDest   
) const;  
DWORD GetTime(  
   CTime& timeDest   
) const;  
DWORD GetTime(  
   LPSYSTEMTIME pTimeDest   
) const;  
```  
  
#### Parameters  
 *timeDest*  
 In the first version, a reference to a [COleDateTime](../vs140/COleDateTime-Class.md) object that will receive the system time information. In the second version, a reference to a [CTime](../Topic/CTime%20Class.md) object that will receive the system time information.  
  
 *pTimeDest*  
 A pointer to the [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure to receive the system time information. Must not be **NULL**.  
  
## Return Value  
 In the first version, nonzero if the time is successfully written to the `COleDateTime` object; otherwise 0. In the second and third versions, a `DWORD` value equal to the **dwFlag** member set in the [NMDATETIMECHANGE](http://msdn.microsoft.com/library/windows/desktop/bb761730) structure. See the **Remarks** section below for more information.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [DTM_GETSYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/bb761769), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. In the MFC implementation of **GetTime**, you can use `COleDateTime` or `CTime` classes, or you can use a `SYSTEMTIME` structure, to store the time information.  
  
 The return value `DWORD` in the second and third versions, above, indicates whether or not the date and time picker control is set to the "no date" status, as indicated in the [NMDATETIMECHANGE](http://msdn.microsoft.com/library/windows/desktop/bb761730) structure member `dwFlags`. If the value returned equals **GDT_NONE**, the control is set to "no date" status, and uses the **DTS_SHOWNONE** style. If the value returned equals **GDT_VALID**, the system time is successfully stored in the destination location.  
  
## Example  
 [!CODE [NVC_MFC_CDateTimeCtrl#5](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl#5)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDateTimeCtrl::SetTime](../vs140/CDateTimeCtrl--SetTime.md)