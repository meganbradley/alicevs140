---
title: "IConnectionPointImpl::Advise"
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
ms.assetid: a54f9487-3ce6-4d29-884b-a50a3ed11b6b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IConnectionPointImpl::Advise
Establishes a connection between the connection point and a sink.  
  
## Syntax  
  
```  
  
      STDMETHOD(Advise)(  
   IUnknown* pUnkSink,  
   DWORD* pdwCookie   
);  
```  
  
## Remarks  
 Use [Unadvise](../vs140/IConnectionPointImpl--Unadvise.md) to terminate the connection call.  
  
 See [IConnectionPoint::Advise](http://msdn.microsoft.com/library/windows/desktop/ms678815) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IConnectionPointImpl Class](../vs140/IConnectionPointImpl-Class.md)