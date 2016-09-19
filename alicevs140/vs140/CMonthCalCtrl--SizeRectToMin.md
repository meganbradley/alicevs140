---
title: "CMonthCalCtrl::SizeRectToMin"
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
ms.assetid: 318bbbe0-ea74-4f0c-bc12-408ed79600bc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMonthCalCtrl::SizeRectToMin
For the current month calendar control, calculates the smallest rectangle that can contain all the calendars that fit in a specified rectangle.  
  
## Syntax  
  
```  
LPRECT SizeRectToMin(  
       LPRECT lpRect  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `lpRect`|Pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that defines a rectangle that contains the desired number of calendars.|  
  
## Return Value  
 Pointer to a [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897) structure that defines a rectangle whose size is less than or equal to the rectangle defined by the `lpRect` parameter.  
  
## Remarks  
 This method calculates how many calendars can fit in the rectangle specified by the `lpRect` parameter, and then returns the smallest rectangle that can contain that number of calendars. In effect, this method shrinks the specified rectangle to exactly fit the desired number of calendars.  
  
 This method sends the [MCM_SIZERECTTOMIN](http://msdn.microsoft.com/library/windows/desktop/bb761020) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdtctl.h  
  
 This control is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CMonthCalCtrl Class](../vs140/CMonthCalCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [MCM_SIZERECTTOMIN](http://msdn.microsoft.com/library/windows/desktop/bb761020)   
 [RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)