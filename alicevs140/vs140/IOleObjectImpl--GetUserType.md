---
title: "IOleObjectImpl::GetUserType"
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
ms.assetid: 59fd615b-5478-4fb1-8da5-29f939c6c957
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::GetUserType
Returns the control's user-type name by calling **OleRegGetUserType**.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetUserType)(  
   DWORD dwFormOfType,  
   LPOLESTR* pszUserType   
);  
```  
  
## Remarks  
 The user-type name is used for display in user-interfaces elements such as menus and dialog boxes. You can change the user-type name in your project's .rgs file.  
  
 See [IOleObject::GetUserType](http://msdn.microsoft.com/library/windows/desktop/ms688643) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [OleRegGetUserType](http://msdn.microsoft.com/library/windows/desktop/ms682271)   
 [IOleObjectImpl::GetUserClassID](../vs140/IOleObjectImpl--GetUserClassID.md)   
 [IOleObjectImpl::GetMiscStatus](../vs140/IOleObjectImpl--GetMiscStatus.md)   
 [IOleObjectImpl::EnumVerbs](../vs140/IOleObjectImpl--EnumVerbs.md)