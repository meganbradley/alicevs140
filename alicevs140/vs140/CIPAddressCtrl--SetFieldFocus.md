---
title: "CIPAddressCtrl::SetFieldFocus"
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
ms.assetid: c14faa58-fde1-47f1-8687-b1dc22780226
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CIPAddressCtrl::SetFieldFocus
Sets the keyboard focus to the specified field in the IP Address Control.  
  
## Syntax  
  
```  
  
      void SetFieldFocus(  
   WORD nField   
);  
```  
  
#### Parameters  
 `nField`  
 Zero-based field index to which the focus should be set. If this value is greater than the number of fields, focus is set to the first blank field. If all fields are non-blank, focus is set to the first field.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [IPM_SETFOCUS](http://msdn.microsoft.com/library/windows/desktop/bb761381), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CIPAddressCtrl Class](../vs140/CIPAddressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CIPAddressCtrl::SetFieldRange](../vs140/CIPAddressCtrl--SetFieldRange.md)