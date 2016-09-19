---
title: "IDispatchImpl::Invoke"
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
ms.assetid: aed01e5a-d6ab-44ef-a33f-0c3d28555bb6
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDispatchImpl::Invoke
Provides access to the methods and properties exposed by the dual interface.  
  
## Syntax  
  
```  
  
      STDMETHOD(Invoke)(  
   DISPID dispidMember,  
   REFIID riid,  
   LCID lcid,  
   WORD wFlags,  
   DISPPARAMS* pdispparams,  
   VARIANT* pvarResult,  
   EXCEPINFO* pexcepinfo,  
   UINT* puArgErr   
);  
```  
  
## Remarks  
 See [IDispatch::Invoke](assetId:///964ade8e-9d8a-4d32-bd47-aa678912a54d) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IDispatchImpl Class](../vs140/IDispatchImpl-Class.md)