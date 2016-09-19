---
title: "IDispEventSimpleImpl::Advise"
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
ms.assetid: c883c0b3-4c05-4ef9-82cc-bb924f6432ca
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IDispEventSimpleImpl::Advise
Call this method to establish a connection with the event source represented by *pUnk*.  
  
## Syntax  
  
```  
  
      HRESULT Advise(  
   IUnknown* pUnk   
);  
```  
  
#### Parameters  
 *pUnk*  
 [in] A pointer to the **IUnknown** interface of the event source object.  
  
## Return Value  
 `S_OK` or any failure `HRESULT` value.  
  
## Remarks  
 Once the connection is established, events fired from *pUnk* will be routed to handlers in your class by way of the event sink map.  
  
> [!NOTE]
>  If your class derives from multiple `IDispEventSimpleImpl` classes, you will need to disambiguate calls to this method by scoping the call with the particular base class you are interested in.  
  
 `Advise` establishes a connection with the default event source, it gets the IID of the default event source of the object as determined by [AtlGetObjectSourceInterface](../vs140/AtlGetObjectSourceInterface.md).  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [IDispEventSimpleImpl Class](../vs140/IDispEventSimpleImpl-Class.md)   
 [IDispEventSimpleImpl::DispEventAdvise](../vs140/IDispEventSimpleImpl--DispEventAdvise.md)   
 [Supporting IDispEventImpl](../vs140/Supporting-IDispEventImpl.md)