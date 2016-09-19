---
title: "IDispEventSimpleImpl::Invoke"
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
ms.assetid: 91441c1f-356d-4b89-9988-fe52b4b4a642
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDispEventSimpleImpl::Invoke
This implementation of **IDispatch::Invoke** calls the event handlers listed in the event sink map.  
  
## Syntax  
  
```  
  
      STDMETHOD(Invoke)(  
   DISPID dispidMember,  
   REFIID /* riid */,  
   LCID lcid,  
   WORD /* wFlags */,  
   DISPPARMS* pdispparams,  
   VARIANT* pvarResult,  
   EXCEPINFO* /* pexcepinfo */,  
   UINT* /* puArgErr */   
);  
```  
  
## Remarks  
 See [IDispatch::Invoke](assetId:///964ade8e-9d8a-4d32-bd47-aa678912a54d).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IDispEventSimpleImpl Class](../vs140/IDispEventSimpleImpl-Class.md)