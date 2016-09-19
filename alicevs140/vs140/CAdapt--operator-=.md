---
title: "CAdapt::operator ="
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
ms.assetid: 7e0087ab-683c-4b36-848a-8bb252aa5d57
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAdapt::operator =
The assignment operator assigns the argument, `rSrc`, to the data member [m_T](../vs140/CAdapt--m_T.md) and returns the current adapter object.  
  
## Syntax  
  
```  
  
      CAdapt& operator=(  
   const T& rSrc   
);  
```  
  
#### Parameters  
 `rSrc`  
 A reference to an object of the adapted type to be copied.  
  
## Return Value  
 A reference to the current object.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CAdapt Class](../vs140/CAdapt-Class.md)   
 [CAdapt::CAdapt](../vs140/CAdapt--CAdapt.md)