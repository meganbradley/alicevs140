---
title: "CAdapt::operator &lt;"
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
ms.assetid: a56f4ddb-3918-4af5-8a93-13bb1f3ed8d9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAdapt::operator &lt;
Compares an object of the adapted type with [m_T](../vs140/CAdapt--m_T.md).  
  
## Syntax  
  
```  
  
      bool operator<(  
   const T& rSrc  
) const;  
```  
  
#### Parameters  
 `rSrc`  
 A reference to the object to be compared.  
  
## Return Value  
 The result of the comparison between `m_T` and `rSrc`.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CAdapt Class](../vs140/CAdapt-Class.md)   
 [CAdapt::operator ==](../vs140/CAdapt--operator-==.md)