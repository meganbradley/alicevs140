---
title: "CButton::SetElevationRequired"
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
ms.assetid: bc5f9c14-1f81-4df2-9058-55834ed67fc3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CButton::SetElevationRequired
Sets the state of the current button control to `elevation required`, which is necessary for the control to display an elevated security icon.  
  
## Syntax  
  
```  
BOOL SetElevationRequired(  
      BOOL fElevationRequired  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `fElevationRequired`|`true` to set `elevation required` state; otherwise, `false`.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 If a button or command link control requires elevated security permission to perform an action, set the control to `elevation required` state. Subsequently, Windows displays the User Account Control (UAC) shield icon on the control. For more information, see "User Account Control" at [MSDN](http://go.microsoft.com/fwlink/?LinkId=18507).  
  
 This method sends the [BCM_SETSHIELD](http://msdn.microsoft.com/library/windows/desktop/bb775979) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CButton Class](../vs140/CButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [BCM_SETSHIELD](http://msdn.microsoft.com/library/windows/desktop/bb775979)