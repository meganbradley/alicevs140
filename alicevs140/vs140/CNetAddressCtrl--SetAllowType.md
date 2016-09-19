---
title: "CNetAddressCtrl::SetAllowType"
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
ms.assetid: f6ceed85-dfde-4b34-be56-9fb3e05198a4
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNetAddressCtrl::SetAllowType
Sets the type of network address that the current network address control can support.  
  
## Syntax  
  
```  
HRESULT SetAllowType(  
     DWORD dwAddrMask  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `dwAddrMask`|A bitwise combination (OR) of flags that specifies the types of addresses the network address control can support. For more information, see [NET_STRING](http://msdn.microsoft.com/library/windows/desktop/bb762586).|  
  
## Return Value  
 `S_OK` if this method is successful; otherwise, a COM error code.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Remarks  
 Use the [CNetAddressCtrl::SetAllowType](../vs140/CNetAddressCtrl--SetAllowType.md) method to specify the types of addresses that the current network address control can support. Use the [CNetAddressCtrl::GetAddress](../vs140/CNetAddressCtrl--GetAddress.md) method to validate and parse the network address that the user enters. Use the [CNetAddressCtrl::DisplayErrorTip](../vs140/CNetAddressCtrl--DisplayErrorTip.md) method to display an error message infotip if the [CNetAddressCtrl::GetAddress](../vs140/CNetAddressCtrl--GetAddress.md) method is unsuccessful.  
  
 This message invokes the [NetAddr_SetAllowType](http://msdn.microsoft.com/library/windows/desktop/bb774320) macro, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. That macro sends the `NCM_SETALLOWTYPE` message.  
  
## See Also  
 [CNetAddressCtrl Class](../vs140/CNetAddressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [NetAddr_SetAllowType](http://msdn.microsoft.com/library/windows/desktop/bb774320)   
 [NET_STRING](http://msdn.microsoft.com/library/windows/desktop/bb762586)   
 [Error Handling (COM)](http://msdn.microsoft.com/library/windows/desktop/ms679692)   
 [CNetAddressCtrl::GetAddress](../vs140/CNetAddressCtrl--GetAddress.md)   
 [CNetAddressCtrl::DisplayErrorTip](../vs140/CNetAddressCtrl--DisplayErrorTip.md)   
 [CNetAddressCtrl::GetAllowType](../vs140/CNetAddressCtrl--GetAllowType.md)