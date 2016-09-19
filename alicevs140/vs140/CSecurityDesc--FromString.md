---
title: "CSecurityDesc::FromString"
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
ms.assetid: 40207261-ac91-467e-9028-f262433cb6b6
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::FromString
Converts a string-format security descriptor into a valid, functional security descriptor.  
  
## Syntax  
  
```  
  
      bool FromString(  
   LPCTSTR pstr   
) throw(...);  
```  
  
#### Parameters  
 `pstr`  
 Pointer to a null-terminated string that contains the [string-format security descriptor](http://msdn.microsoft.com/library/windows/desktop/aa379570) to be converted.  
  
## Return Value  
 Returns true on success. Throws an exception on failure.  
  
## Remarks  
 The string can be created by using [CSecurityDesc::ToString](../vs140/CSecurityDesc--ToString.md). Converting the security descriptor into a string makes it easier to store and transmit.  
  
 This method is only available with Windows 2000 and later because it calls [ConvertStringSecurityDescriptorToSecurityDescriptor](http://msdn.microsoft.com/library/windows/desktop/aa376401).  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [ConvertSecurityDescriptorToStringSecurityDescriptor](http://msdn.microsoft.com/library/windows/desktop/aa376397)   
 [SECURITY_DESCRIPTOR](http://msdn.microsoft.com/library/windows/desktop/aa379561)   
 [CSecurityDesc::ToString](../vs140/CSecurityDesc--ToString.md)