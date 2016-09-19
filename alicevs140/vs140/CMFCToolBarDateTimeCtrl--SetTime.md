---
title: "CMFCToolBarDateTimeCtrl::SetTime"
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
ms.assetid: 6b12e277-a80c-4156-8913-67358b9630b1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::SetTime
Sets the time and date in the time picker control.  
  
## Syntax  
  
```  
BOOL SetTime(  
   const COleDateTime& timeNew   
);  
BOOL SetTime(  
   const CTime* timeNew   
);  
BOOL SetTime(  
   LPSYSTEMTIME pTimeNew=NULL   
);  
```  
  
#### Parameters  
 `[in] timeNew`  
 In the first version, a reference to a [COleDateTime](../vs140/COleDateTime-Class.md) object that contains the time to which the control will be set. In the second version, a pointer to a [CTime](../Topic/CTime%20Class.md) object that contains the time to which the control will be set.  
  
 `[in] pTimeNew`  
 A pointer to the [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure that contains the time to which the control will be set.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Sets the time in a date and time picker control by calling [CDateTimeCtrl::SetTime](../vs140/CDateTimeCtrl--SetTime.md).  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)