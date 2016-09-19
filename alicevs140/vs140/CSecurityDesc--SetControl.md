---
title: "CSecurityDesc::SetControl"
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
ms.assetid: d0f59825-c49c-4d19-9f00-152d6a7d20d6
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSecurityDesc::SetControl
Sets the control bits of a security descriptor.  
  
## Syntax  
  
```  
bool SetControl(  
   SECURITY_DESCRIPTOR_CONTROL ControlBitsOfInterest,  
   SECURITY_DESCRIPTOR_CONTROL ControlBitsToSet   
) throw( );  
```  
  
#### Parameters  
 `ControlBitsOfInterest`  
 A **SECURITY_DESCRIPTOR_CONTROL** mask that indicates the control bits to set. For a list of the flags which can be set, see [SetSecurityDescriptorControl](http://msdn.microsoft.com/library/windows/desktop/aa379582\(v=vs.85\).aspx).  
  
 `ControlBitsToSe`t  
 A `SECURITY_DESCRIPTOR_CONTROL` mask that indicates the new values for the control bits specified by the `ControlBitsOfInterest` mask. This parameter can be a combination of the flags listed for the `ControlBitsOfInterest` parameter.  
  
## Return Value  
 Returns true on success, false on failure.  
  
## Remarks  
 This method is available only on Windows 2000 and later, as it calls [SetSecurityDescriptorControl](http://msdn.microsoft.com/library/windows/desktop/aa379582\(v=vs.85\).aspx).  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CSecurityDesc Class](../vs140/CSecurityDesc-Class.md)   
 [CSecurityDesc::SetDacl](../vs140/CSecurityDesc--SetDacl.md)   
 [CSecurityDesc::SetGroup](../vs140/CSecurityDesc--SetGroup.md)   
 [CSecurityDesc::SetOwner](../vs140/CSecurityDesc--SetOwner.md)   
 [CSecurityDesc::SetSacl](../vs140/CSecurityDesc--SetSacl.md)   
 [CSecurityDesc::GetControl](../vs140/CSecurityDesc--GetControl.md)