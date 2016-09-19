---
title: "CNetAddressCtrl::GetAddress"
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
ms.assetid: b5aadf4e-3fd7-4e21-8064-4a83daefbae7
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNetAddressCtrl::GetAddress
Retrieves a validated and parsed representation of the network address that is associated with the current network address control.  
  
## Syntax  
  
```  
HRESULT GetAddress(  
        PNC_ADDRESS pAddress   
 ) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in, out] `pAddress`|Pointer to an [NC_ADDRESS](http://msdn.microsoft.com/library/windows/desktop/bb773345) structure.  Set the `pAddrInfo` member of this structure to the address of a [NET_ADDRESS_INFO](http://msdn.microsoft.com/library/windows/desktop/bb773346) structure before you call the GetAddress method.|  
  
## Return Value  
 The value `S_OK` if this method is successful; otherwise, a COM error code. For more information about the possible error codes, see the Return Value section of the [NetAddr_GetAddress](http://msdn.microsoft.com/library/windows/desktop/bb774316) macro.  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Remarks  
 If this method is successful, the [NET_ADDRESS_INFO](http://msdn.microsoft.com/library/windows/desktop/bb773346) structure contains additional information about the network address.  
  
 Use the [CNetAddressCtrl::SetAllowType](../vs140/CNetAddressCtrl--SetAllowType.md) method to specify the types of addresses the current network address control can support. Use the [CNetAddressCtrl::GetAddress](../vs140/CNetAddressCtrl--GetAddress.md) method to validate and parse the network address that the user enters. Use the [CNetAddressCtrl::DisplayErrorTip](../vs140/CNetAddressCtrl--DisplayErrorTip.md) method to display an error message infotip if the [CNetAddressCtrl::GetAddress](../vs140/CNetAddressCtrl--GetAddress.md) method is unsuccessful.  
  
 This method invokes the [NetAddr_GetAddress](http://msdn.microsoft.com/library/windows/desktop/bb774316) macro, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. That macro sends the `NCM_GETADDRESS` message.  
  
## See Also  
 [CNetAddressCtrl Class](../vs140/CNetAddressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [NetAddr_GetAddress Macro](http://msdn.microsoft.com/library/windows/desktop/bb774316)   
 [CNetAddressCtrl::SetAllowType](../vs140/CNetAddressCtrl--SetAllowType.md)   
 [CNetAddressCtrl::DisplayErrorTip](../vs140/CNetAddressCtrl--DisplayErrorTip.md)   
 [Error Handling (COM)](http://msdn.microsoft.com/library/windows/desktop/ms679692)