---
title: "CRegKey::Open"
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
ms.assetid: 15f43aff-752d-4784-a223-1e14ac402fe3
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::Open
Call this method to open the specified key and set [m_hKey](../vs140/CRegKey--m_hKey.md) to the handle of this key.  
  
## Syntax  
  
```  
  
      LONG Open(  
   HKEY hKeyParent,  
   LPCTSTR lpszKeyName,  
   REGSAM samDesired = KEY_READ | KEY_WRITE  
) throw( );  
```  
  
#### Parameters  
 `hKeyParent`  
 The handle of an open key.  
  
 `lpszKeyName`  
 Specifies the name of a key to be created or opened. This name must be a subkey of `hKeyParent`.  
  
 `samDesired`  
 The security access for the key. The default value is KEY_ALL_ACCESS. For a list of possible values and descriptions, see [RegCreateKeyEx](http://msdn.microsoft.com/library/windows/desktop/ms724844) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Return Value  
 If successful, returns ERROR_SUCCESS; otherwise, a non-zero error value defined in WINERROR.H.  
  
## Remarks  
 If the `lpszKeyName` parameter is NULL or points to an empty string, **Open** opens a new handle of the key identified by `hKeyParent`, but does not close any previously opened handle.  
  
 Unlike [CRegKey::Create](../vs140/CRegKey--Create.md), **Open** will not create the specified key if it does not exist.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::Close](../vs140/CRegKey--Close.md)