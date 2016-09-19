---
title: "CMFCToolBarDateTimeCtrl::SetTimeAll"
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
ms.assetid: b5bf63c3-447c-444f-9cc6-7f31ce60b111
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarDateTimeCtrl::SetTimeAll
Sets the time and date in all instances of the time picker control that have a specified command ID.  
  
## Syntax  
  
```  
static BOOL SetTimeAll(  
   UINT uiCmd,  
   const COleDateTime& timeNew   
);  
static BOOL SetTimeAll(  
   UINT uiCmd,  
   const CTime* pTimeNew   
);  
static BOOL SetTimeAll(  
   UINT uiCmd,  
   LPSYSTEMTIME pTimeNew=NULL   
);  
```  
  
#### Parameters  
 `[in] uiCmd`  
 Specifies a toolbar button's command ID.  
  
 `[in] timeNew`  
 In the first version, a [COleDateTime](../vs140/COleDateTime-Class.md) object that contains the time to which the control will be set. In the second version, a pointer to a [CTime](../Topic/CTime%20Class.md) object that contains the time to which the control will be set.  
  
 `[in] pTimeNew`  
 A pointer to the [SYSTEMTIME](http://msdn.microsoft.com/library/windows/desktop/ms724950) structure that contains the time to which the control will be set.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 Looks for a toolbar button with the specified command ID and sets the time in a date and time picker control by calling [CMFCToolBarDateTimeCtrl::SetTime](../vs140/CMFCToolBarDateTimeCtrl--SetTime.md).  
  
## Requirements  
 **Header:** afxtoolbardatetimectrl.h  
  
## See Also  
 [CMFCToolBarDateTimeCtrl Class](../vs140/CMFCToolBarDateTimeCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)