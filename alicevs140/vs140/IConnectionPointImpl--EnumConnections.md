---
title: "IConnectionPointImpl::EnumConnections"
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
ms.assetid: e58182eb-6b82-42d9-a156-8b0b74cd54f7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IConnectionPointImpl::EnumConnections
Creates an enumerator to iterate through the connections for the connection point.  
  
## Syntax  
  
```  
  
      STDMETHOD(EnumConnections)(  
   IEnumConnections** ppEnum   
);  
```  
  
## Remarks  
 See [IConnectionPoint::EnumConnections](http://msdn.microsoft.com/library/windows/desktop/ms680755) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IConnectionPointImpl Class](../vs140/IConnectionPointImpl-Class.md)   
 [IEnumConnections](http://msdn.microsoft.com/library/windows/desktop/ms682237)