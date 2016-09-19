---
title: "CA2WEX::CA2WEX"
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
ms.assetid: 5a52da38-0a57-4baf-b2e4-6963f11205c4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CA2WEX::CA2WEX
The constructor.  
  
## Syntax  
  
```  
  
      CA2WEX(  
   LPCSTR psz,  
   UINT nCodePage  
) throw(...);  
CA2WEX(  
   LPCSTR psz  
) throw(...);  
```  
  
#### Parameters  
 `psz`  
 The text string to be converted.  
  
 `nCodePage`  
 The code page used to perform the conversion. See the code page parameter discussion for the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] function [MultiByteToWideChar](http://msdn.microsoft.com/library/windows/desktop/dd319072) for more details.  
  
## Remarks  
 Allocates the buffer used in the translation process.  
  
## Requirements  
 **Header:** atlconv.h  
  
## See Also  
 [CA2WEX Class](../vs140/CA2WEX-Class.md)