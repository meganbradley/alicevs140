---
title: "CIPAddressCtrl::IsBlank"
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
ms.assetid: e26c49f2-23ce-4706-b75f-33f906d45c42
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CIPAddressCtrl::IsBlank
Determines if all fields in the IP Address Control are empty.  
  
## Syntax  
  
```  
  
BOOL IsBlank( ) const;  
  
```  
  
## Return Value  
 Nonzero if all of the IP Address Control fields are empty; otherwise 0.  
  
## Remarks  
 This member function implements the behavior of the Win32 message [IPM_ISBLANK](http://msdn.microsoft.com/library/windows/desktop/bb761379), as described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CIPAddressCtrl Class](../vs140/CIPAddressCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)