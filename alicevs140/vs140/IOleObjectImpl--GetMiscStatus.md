---
title: "IOleObjectImpl::GetMiscStatus"
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
ms.assetid: 4cdaf66b-265c-484e-847b-617560f0fd7a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::GetMiscStatus
Returns a pointer to registered status information for the control by calling **OleRegGetMiscStatus**.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetMiscStatus)(  
   DWORD dwAspect,  
   DWORD* pdwStatus   
);  
```  
  
## Remarks  
 The status information includes behaviors supported by the control and presentation data. You can add status information to your project's .rgs file.  
  
 See [IOleObject::GetMiscStatus](http://msdn.microsoft.com/library/windows/desktop/ms678521) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [OleRegGetMiscStatus](http://msdn.microsoft.com/library/windows/desktop/ms680124)   
 [IOleObjectImpl::EnumVerbs](../vs140/IOleObjectImpl--EnumVerbs.md)   
 [IOleObjectImpl::GetUserType](../vs140/IOleObjectImpl--GetUserType.md)