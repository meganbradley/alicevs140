---
title: "CMonthCalCtrl::GetCalID"
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
ms.assetid: 7867c65d-52b5-4a0b-8f71-abc0152d56a1
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::GetCalID
Retrieves the calendar identifier for the current month calendar control.  
  
## Syntax  
  
```  
CALID GetCalID() const;  
```  
  
## Return Value  
 One of the [calendar identifier](http://msdn.microsoft.com/library/windows/desktop/dd317732) constants.  
  
## Remarks  
 A calendar identifier denotes a region-specific calendar, such as the Gregorian (localized), Japanese, or Hijri calendars. Your application can use a calendar identifier that has various language support functions.  
  
 This method sends the [MCM_GETCALID](http://msdn.microsoft.com/library/windows/desktop/bb760951) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_GETCALID](http://msdn.microsoft.com/library/windows/desktop/bb760951)   
 [Calendar Identifiers](http://msdn.microsoft.com/library/windows/desktop/dd317732)   
 [CMonthCalCtrl::SetCalID](../vs140/CMonthCalCtrl--SetCalID.md)