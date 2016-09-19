---
title: "CAdapt::operator const T&amp;"
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
ms.assetid: 03ae2e9f-22fd-4db8-8b41-86fd269bdad2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAdapt::operator const T&amp;
Returns a **const** reference to the [m_T](../vs140/CAdapt--m_T.md) member, allowing the adapter object to be treated as if it were an object of type `T`.  
  
## Syntax  
  
```  
  
operator const T&( ) const;  
  
```  
  
## Return Value  
 A **const** reference to `m_T`.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CAdapt Class](../vs140/CAdapt-Class.md)   
 [CAdapt::operator T&](../vs140/CAdapt--operator-T-.md)