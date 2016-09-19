---
title: "IConnectionPointContainerImpl::FindConnectionPoint"
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
ms.assetid: 8d655710-8fba-46d0-a2d1-b92da74e5825
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IConnectionPointContainerImpl::FindConnectionPoint
Retrieves an interface pointer to the connection point that supports the specified IID.  
  
## Syntax  
  
```  
  
      STDMETHOD(FindConnectionPoint)(  
   REFIID riid,  
   IConnectionPoint** ppCP   
);  
```  
  
## Remarks  
 See [IConnectionPointContainer::FindConnectionPoint](http://msdn.microsoft.com/library/windows/desktop/ms692476) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IConnectionPointContainerImpl Class](../vs140/IConnectionPointContainerImpl-Class.md)   
 [IConnectionPointImpl Class](../vs140/IConnectionPointImpl-Class.md)