---
title: "IConnectionPointImpl::GetConnectionPointContainer"
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
ms.assetid: 46af1c75-62cf-408c-8c8c-c09c7ab5e6eb
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IConnectionPointImpl::GetConnectionPointContainer
Retrieves an interface pointer to the connectable object.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetConnectionPointContainer)(  
   IConnectionPointContainer** ppCPC   
);  
```  
  
## Remarks  
 See [IConnectionPoint::GetConnectionPointContainer](http://msdn.microsoft.com/library/windows/desktop/ms679669) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IConnectionPointImpl Class](../vs140/IConnectionPointImpl-Class.md)   
 [IConnectionPointContainerImpl Class](../vs140/IConnectionPointContainerImpl-Class.md)