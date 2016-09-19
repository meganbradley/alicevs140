---
title: "CNetAddressCtrl::GetAllowType"
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
ms.assetid: a9cf299f-aafd-4a0a-aa8d-ba7c589b4183
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CNetAddressCtrl::GetAllowType
Retrieves the type of network address that the current network address control can support.  
  
## Syntax  
  
```  
DWORD GetAllowType() const;  
```  
  
## Return Value  
 A bitwise combination (OR) of flags that specifies the types of addresses the network address control can support. For more information, see [NET_STRING](http://msdn.microsoft.com/library/windows/desktop/bb762586).  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## Remarks  
 This message invokes the [NetAddr_GetAllowType](http://msdn.microsoft.com/library/windows/desktop/bb774318) macro, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. That macro sends the `NCM_GETALLOWTYPE` message.  
  
## See Also  
 [CNetAddressCtrl Class](../vs140/CNetAddressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [NetAddr_GetAllowType](http://msdn.microsoft.com/library/windows/desktop/bb774318)   
 [CNetAddressCtrl::SetAllowType](../vs140/CNetAddressCtrl--SetAllowType.md)   
 [NET_STRING](http://msdn.microsoft.com/library/windows/desktop/bb762586)