---
title: "CDateTimeCtrl::SetTime"
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
ms.assetid: 52e058b3-581a-47e3-8c70-19138fac90b6
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDateTimeCtrl::SetTime
Sets the time in a date and time picker control.  
  
## Syntax  
  
```  
  
      BOOL SetTime(  
   const COleDateTime& timeNew   
);  
BOOL SetTime(  
   const CTime* pTimeNew   
);  
BOOL SetTime(  
   LPSYSTEMTIME pTimeNew = NULL   
);  
```  
  
#### Parameters  
 *timeNew*  
 A reference to a [COleDateTime](../vs140/COleDateTime-Class.md) object containing the to which the control will be set.  
  
 *pTimeNew*  
 In the second version above, a pointer to a [CTime](../Topic/CTime%20Class.md) object containing the time to which the control will be set. In the third version above, a pointer to a [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure containing the time to which the control will be set.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [DTM_SETSYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/bb761782), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. In the MFC implementation of **SetTime**, you can use the `COleDateTime` or `CTime` classes, or you can use a `SYSTEMTIME` structure, to set the time information.  
  
## Example  
 [!CODE [NVC_MFC_CDateTimeCtrl#8](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CDateTimeCtrl#8)]  
  
## Requirements  
 **Header:** afxdtctl.h  
  
## See Also  
 [CDateTimeCtrl Class](../vs140/CDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDateTimeCtrl::GetTime](../vs140/CDateTimeCtrl--GetTime.md)