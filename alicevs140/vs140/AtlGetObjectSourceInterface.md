---
title: "AtlGetObjectSourceInterface"
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
ms.assetid: a8528f45-fbfb-4e24-ad1a-1d69b2897155
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlGetObjectSourceInterface
Call this function to retrieve information about the default source interface of an object.  
  
> [!IMPORTANT]
>  This function cannot be used in applications that execute in the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
  
      ATLAPI AtlGetObjectSourceInterface(  
IUnknown* punkObj,  
GUID* plibid,  
IID* piid,  
unsigned short* pdwMajor,  
unsigned short* pdwMinor  
);  
```  
  
#### Parameters  
 `punkObj`  
 [in] A pointer to the object for which information is to be returned.  
  
 `plibid`  
 [out] A pointer to the LIBID of the type library containing the definition of the source interface.  
  
 `piid`  
 [out] A pointer to the interface ID of the object's default source interface.  
  
 *pdwMajor*  
 [out] A pointer to the major version number of the type library containing the definition of the source interface.  
  
 *pdwMinor*  
 [out] A pointer to the minor version number of the type library containing the definition of the source interface.  
  
## Return Value  
 A standard HRESULT value.  
  
## Remarks  
 `AtlGetObjectSourceInterface` can provide you with the interface ID of the default source interface, along with the LIBID and major and minor version numbers of the type library describing that interface.  
  
> [!NOTE]
>  For this function to successfully retrieve the requested information, the object represented by `punkObj` must implement `IDispatch` (and return type information through **IDispatch::GetTypeInfo**) plus it must also implement either `IProvideClassInfo2` or `IPersist`. The type information for the source interface must be in the same type library as the type information for `IDispatch`.  
  
## Example  
 The example below shows how you might define an event sink class, `CEasySink`, that reduces the number of template arguments that you can pass to `IDispEventImpl` to the bare essentials. `EasyAdvise` and `EasyUnadvise` use `AtlGetObjectSourceInterface` to initialize the [IDispEventImpl](../vs140/IDispEventImpl-Class.md) members before calling [DispEventAdvise](../vs140/IDispEventSimpleImpl--DispEventAdvise.md) or [DispEventUnadvise](../vs140/IDispEventSimpleImpl--DispEventUnadvise.md).  
  
 [!CODE [NVC_ATL_Windowing#93](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#93)]  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [Composite Control Global Functions](../vs140/Composite-Control-Global-Functions.md)   
 [IDispEventImpl Class](../vs140/IDispEventImpl-Class.md)   
 [IDispEventSimpleImpl Class](../vs140/IDispEventSimpleImpl-Class.md)