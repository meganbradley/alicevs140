---
title: "CComPtrBase::Release"
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
ms.assetid: b20c9def-26fd-4197-ae83-769207d9b346
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPtrBase::Release
Call this method to release the interface.  
  
## Syntax  
  
```  
  
void Release( ) throw( );  
  
```  
  
## Remarks  
 The interface is released, and [CComPtrBase::p](../vs140/CComPtrBase--p.md) is set to NULL.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComPtrBase Class](../vs140/CComPtrBase-Class.md)