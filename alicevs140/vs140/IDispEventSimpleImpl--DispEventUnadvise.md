---
title: "IDispEventSimpleImpl::DispEventUnadvise"
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
ms.assetid: dca9e50a-89bd-4643-82ba-a692087e9dda
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDispEventSimpleImpl::DispEventUnadvise
Breaks the connection with the event source represented by *pUnk*.  
  
## Syntax  
  
```  
  
      HRESULT DispEventUnadvise(  
   IUnknown* pUnk   
   const IID* piid   
);  
```  
  
#### Parameters  
 *pUnk*  
 [in] A pointer to the **IUnknown** interface of the event source object.  
  
 `piid`  
 A pointer to the IID of the event source object.  
  
## Return Value  
 `S_OK` or any failure `HRESULT` value.  
  
## Remarks  
 Once the connection is broken, events will no longer be routed to the handler functions listed in the event sink map.  
  
> [!NOTE]
>  If your class derives from multiple `IDispEventSimpleImpl` classes, you will need to disambiguate calls to this method by scoping the call with the particular base class you are interested in.  
  
 `DispEventAdvise` breaks a connection that was established with the event source specified in `pdiid`.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IDispEventSimpleImpl Class](../vs140/IDispEventSimpleImpl-Class.md)   
 [Supporting IDispEventImpl](../vs140/Supporting-IDispEventImpl.md)