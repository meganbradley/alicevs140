---
title: "IDispEventImpl::GetFuncInfoFromId"
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
ms.assetid: ef443397-699b-4874-ab13-7465c22a479d
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDispEventImpl::GetFuncInfoFromId
Locates the function index for the specified dispatch identifier.  
  
## Syntax  
  
```  
  
      HRESULT GetFuncInfoFromId(  
   const IID& iid,  
   DISPID dispidMember,  
   LCID lcid,  
   _ATL_FUNC_INFO& info   
);  
```  
  
#### Parameters  
 `iid`  
 [in] A reference to the ID of the function.  
  
 *dispidMember*  
 [in] The dispatch ID of the function.  
  
 `lcid`  
 [in] The locale context of the function ID.  
  
 `info`  
 [in] The structure indicating how the function is called.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IDispEventImpl Class](../vs140/IDispEventImpl-Class.md)   
 [Supporting IDispEventImpl](../vs140/Supporting-IDispEventImpl.md)