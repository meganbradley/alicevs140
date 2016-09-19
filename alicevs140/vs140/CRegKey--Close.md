---
title: "CRegKey::Close"
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
ms.assetid: 480cf95f-7eb1-4c26-bb21-561ac9be793c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRegKey::Close
Call this method to release the [m_hKey](../vs140/CRegKey--m_hKey.md) member handle and set it to NULL.  
  
## Syntax  
  
```  
  
LONG Close( ) throw( );  
  
```  
  
## Return Value  
 If successful, returns ERROR_SUCCESS; otherwise returns an error value.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CRegKey Class](../vs140/CRegKey-Class.md)   
 [CRegKey::Open](../vs140/CRegKey--Open.md)