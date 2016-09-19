---
title: "IOleObjectImpl::EnumAdvise"
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
ms.assetid: 18b667e2-6b7f-41ad-9a5b-a5b74408c043
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::EnumAdvise
Supplies an enumeration of registered advisory connections for this control.  
  
## Syntax  
  
```  
  
      STDMETHOD(EnumAdvise)(  
   IEnumSTATDATA** ppenumAdvise   
);  
```  
  
## Remarks  
 See [IOleObject::EnumAdvise](http://msdn.microsoft.com/library/windows/desktop/ms682355) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [IOleObjectImpl::EnumVerbs](../vs140/IOleObjectImpl--EnumVerbs.md)