---
title: "IOleObjectImpl::SetHostNames"
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
ms.assetid: 6d71b539-8ca6-4613-942c-ae38157ed957
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::SetHostNames
Tells the control the names of the container application and container document.  
  
## Syntax  
  
```  
  
      STDMETHOD(SetHostNames)(  
   LPCOLESTR /* szContainerApp */,  
   LPCOLESTR /* szContainerObj */  
);  
```  
  
## Return Value  
 Returns `S_OK`.  
  
## Remarks  
 See [IOleObject::SetHostNames](http://msdn.microsoft.com/library/windows/desktop/ms680642) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)