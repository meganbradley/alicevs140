---
title: "CW2AEX::CW2AEX"
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
ms.assetid: 3cf73bf7-091b-45c6-bc17-c4c733156f80
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CW2AEX::CW2AEX
The constructor.  
  
## Syntax  
  
```  
  
      CW2AEX(  
   LPCWSTR psz,  
   UINT nCodePage  
) throw(...);  
CW2AEX(  
   LPCWSTR psz  
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
 [CW2AEX Class](../vs140/CW2AEX-Class.md)