---
title: "CNetAddressCtrl::DisplayErrorTip"
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
ms.assetid: 02176102-f107-40c5-a6ae-d28e82b264ae
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNetAddressCtrl::DisplayErrorTip
Displays an error message in the balloon tip that is associated with the current network address control.  
  
## Syntax  
  
```  
HRESULT DisplayErrorTip();  
```  
  
## Return Value  
 The value `S_OK` if this method is successful; otherwise, an error code.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Remarks  
 Use the [CNetAddressCtrl::SetAllowType](../vs140/CNetAddressCtrl--SetAllowType.md) method to specify the types of addresses that the current network address control can support. Use the [CNetAddressCtrl::GetAddress](../vs140/CNetAddressCtrl--GetAddress.md) method to validate and parse the network address that the user enters. Use the [CNetAddressCtrl::DisplayErrorTip](../vs140/CNetAddressCtrl--DisplayErrorTip.md) method to display an error message infotip if the [CNetAddressCtrl::GetAddress](../vs140/CNetAddressCtrl--GetAddress.md) method is unsuccessful.  
  
 This message invokes the [NetAddr_DisplayErrorTip](http://msdn.microsoft.com/library/windows/desktop/bb774314) macro, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. That macro sends the `NCM_DISPLAYERRORTIP` message.  
  
## See Also  
 [CNetAddressCtrl Class](../vs140/CNetAddressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [NetAddr_DisplayErrorTip](http://msdn.microsoft.com/library/windows/desktop/bb774314)   
 [CNetAddressCtrl::SetAllowType](../vs140/CNetAddressCtrl--SetAllowType.md)   
 [CNetAddressCtrl::GetAddress](../vs140/CNetAddressCtrl--GetAddress.md)