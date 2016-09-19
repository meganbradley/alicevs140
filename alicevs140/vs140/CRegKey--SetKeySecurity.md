---
title: "CRegKey::SetKeySecurity"
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
ms.assetid: 7d66dcb3-2a59-48ab-976c-bc96f1ab667c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::SetKeySecurity
Call this method to set the security of the registry key.  
  
## Syntax  
  
```  
  
      LONG SetKeySecurity(  
   SECURITY_INFORMATION si,  
   PSECURITY_DESCRIPTOR psd   
) throw( );  
```  
  
#### Parameters  
 `si`  
 Specifies the components of the security descriptor to set. The value can be a combination of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|DACL_SECURITY_INFORMATION|Sets the key's discretionary access-control list (DACL). The key must have WRITE_DAC access, or the calling process must be the object's owner.|  
|GROUP_SECURITY_INFORMATION|Sets the key's primary group security identifier (SID). The key must have WRITE_OWNER access, or the calling process must be the object's owner.|  
|OWNER_SECURITY_INFORMATION|Sets the key's owner SID. The key must have WRITE_OWNER access, or the calling process must be the object's owner or have the SE_TAKE_OWNERSHIP_NAME privilege enabled.|  
|SACL_SECURITY_INFORMATION|Sets the key's system access-control list (SACL). The key must have ACCESS_SYSTEM_SECURITY access. The proper way to get this access is to enable the SE_SECURITY_NAME [privilege](http://msdn.microsoft.com/library/windows/desktop/aa379306) in the caller's current access token, open the handle for ACCESS_SYSTEM_SECURITY access, and then disable the privilege.|  
  
 `psd`  
 Pointer to a [SECURITY_DESCRIPTOR](http://msdn.microsoft.com/library/windows/desktop/aa379561) structure that specifies the security attributes to set for the specified key.  
  
## Return Value  
 If the method succeeds, the return value is ERROR_SUCCESS. If the method fails, the return value is a nonzero error code defined in WINERROR.H.  
  
## Remarks  
 Sets the key's security attributes. See [RegSetKeySecurity](http://msdn.microsoft.com/library/windows/desktop/aa379314) for more details.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::GetKeySecurity](../vs140/CRegKey--GetKeySecurity.md)