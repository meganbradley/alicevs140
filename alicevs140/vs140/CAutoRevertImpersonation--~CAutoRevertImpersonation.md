---
title: "CAutoRevertImpersonation::~CAutoRevertImpersonation"
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
ms.assetid: 741b4a9f-2741-4a9b-846e-c6f4670b5d11
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAutoRevertImpersonation::~CAutoRevertImpersonation
Destroys the object and reverts access token impersonation.  
  
## Syntax  
  
```  
  
~CAutoRevertImpersonation() throw( );  
  
```  
  
## Remarks  
 Reverts any impersonation currently in effect for the [CAccessToken](../vs140/CAccessToken-Class.md) object provided either at construction or through the [Attach](../vs140/CAutoRevertImpersonation--Attach.md) method. If no `CAccessToken` is associated, the destructor has no effect.  
  
## Requirements  
 **Header:** atlsecurity.h  
  
## See Also  
 [CAutoRevertImpersonation Class](../vs140/CAutoRevertImpersonation-Class.md)   
 [CAccessToken Class](../vs140/CAccessToken-Class.md)