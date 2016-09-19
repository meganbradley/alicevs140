---
title: "CIPAddressCtrl::SetFieldRange"
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
ms.assetid: f6f9067c-c0f3-400a-b1f7-582b58bcf023
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CIPAddressCtrl::SetFieldRange
Sets the range in the specified field in the IP Address Control.  
  
## Syntax  
  
```  
  
      void SetFieldRange(  
   int nField,  
   BYTE nLower,  
   BYTE nUpper   
);  
```  
  
#### Parameters  
 `nField`  
 Zero-based field index to which the range will be applied.  
  
 `nLower`  
 A reference to an integer receiving the lower limit of the specified field in this IP Address Control.  
  
 `nUpper`  
 A reference to an integer receiving the upper limit of the specified field in this IP Address Control.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [IPM_SETRANGE](http://msdn.microsoft.com/library/windows/desktop/bb761382), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. Use the two parameters, `nLower` and `nUpper`, to indicate the lower and upper limits of the field, instead of the *wRange* parameter used with the Win32 message.  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CIPAddressCtrl Class](../vs140/CIPAddressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CIPAddressCtrl::SetFieldFocus](../vs140/CIPAddressCtrl--SetFieldFocus.md)