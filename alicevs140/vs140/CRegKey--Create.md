---
title: "CRegKey::Create"
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
ms.assetid: 18526952-335f-4cd1-88c7-aa001c6c184b
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::Create
Call this method to create the specified key, if it does not exist as a subkey of `hKeyParent`.  
  
## Syntax  
  
```  
  
      LONG Create(  
   HKEY hKeyParent,  
   LPCTSTR lpszKeyName,  
   LPTSTR lpszClass = REG_NONE,  
   DWORD dwOptions = REG_OPTION_NON_VOLATILE,  
   REGSAM samDesired = KEY_READ | KEY_WRITE,  
   LPSECURITY_ATTRIBUTES lpSecAttr = NULL,  
   LPDWORD lpdwDisposition = NULL   
) throw( );  
```  
  
#### Parameters  
 `hKeyParent`  
 The handle of an open key.  
  
 `lpszKeyName`  
 Specifies the name of a key to be created or opened. This name must be a subkey of `hKeyParent`.  
  
 `lpszClass`  
 Specifies the class of the key to be created or opened. The default value is REG_NONE.  
  
 `dwOptions`  
 Options for the key. The default value is REG_OPTION_NON_VOLATILE. For a list of possible values and descriptions, see [RegCreateKeyEx](http://msdn.microsoft.com/library/windows/desktop/ms724844) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `samDesired`  
 The security access for the key. The default value is KEY_READ &#124; KEY_WRITE. For a list of possible values and descriptions, see **RegCreateKeyEx**.  
  
 *lpSecAttr*  
 A pointer to a [SECURITY_ATTRIBUTES](http://msdn.microsoft.com/library/windows/desktop/aa379560) structure that indicates whether the handle of the key can be inherited by a child process. By default, this parameter is NULL (meaning the handle cannot be inherited).  
  
 *lpdwDisposition*  
 [out] If non-NULL, retrieves either REG_CREATED_NEW_KEY (if the key did not exist and was created) or REG_OPENED_EXISTING_KEY (if the key existed and was opened).  
  
## Return Value  
 If successful, returns ERROR_SUCCESS and opens the key. If the method fails, the return value is a nonzero error code defined in WINERROR.H.  
  
## Remarks  
 **Create** sets the [m_hKey](../vs140/CRegKey--m_hKey.md) member to the handle of this key.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::Open](../vs140/CRegKey--Open.md)   
 [CRegKey::Close](../vs140/CRegKey--Close.md)