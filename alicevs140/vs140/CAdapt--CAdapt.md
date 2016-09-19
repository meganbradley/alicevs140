---
title: "CAdapt::CAdapt"
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
ms.assetid: 4527726f-a413-4021-b2e6-854e7a8a3322
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAdapt::CAdapt
The constructors allow an adapter object to be default constructed, copied from an object of the adapted type, or copied from another adapter object.  
  
## Syntax  
  
```  
  
      CAdapt( );   
CAdapt(  
   const T& rSrc   
);  
CAdapt(  
   const CAdapt& rSrCA   
);  
```  
  
#### Parameters  
 `rSrc`  
 A variable of the type being adapted to be copied into the newly constructed adapter object.  
  
 *rSrCA*  
 An adapter object whose contained data should be copied into the newly constructed adapter object.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CAdapt Class](../vs140/CAdapt-Class.md)   
 [CAdapt::operator =](../vs140/CAdapt--operator-=.md)