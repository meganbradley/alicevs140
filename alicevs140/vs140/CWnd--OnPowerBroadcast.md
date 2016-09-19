---
title: "CWnd::OnPowerBroadcast"
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
ms.assetid: e5a79a17-1aeb-41f8-9e06-76e8f4223b99
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnPowerBroadcast
The framework calls this member function when a power-management event occurs.  
  
## Syntax  
  
```  
afx_msg UINT OnPowerBroadcast(  
    UINT nPowerEvent,   
    UINT nEventData  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `nPowerEvent`|The power-management event.|  
|[in] `nEventData`|Event-specific data.|  
  
## Return Value  
 If the event is a request, return `true` to grant the request, or `BROADCAST_QUERY_DENY` to deny the request.  
  
## Remarks  
 This method receives the [WM_POWERBROADCAST](http://msdn.microsoft.com/library/windows/desktop/aa373247) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 The `nPowerEvent` parameter specifies events such as battery power is low, the power status has changed, permission to suspend operation is requested or denied, an operation is resuming automatically after an event, the system is suspending operation, or an operation is resuming after suspension. The `nEventData` parameter is typically not used. For more information, see the `wParam` and `lParam` parameters of the [WM_POWERBROADCAST](http://msdn.microsoft.com/library/windows/desktop/aa373247) message.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [WM_POWERBROADCAST](http://msdn.microsoft.com/library/windows/desktop/aa373247)