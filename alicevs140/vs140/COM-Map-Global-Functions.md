---
title: "COM Map Global Functions"
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
ms.assetid: b9612d30-eb23-46ef-8093-d56f237d3cf1
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COM Map Global Functions
These functions provide support for COM Map             **IUnknown** implementations.  
  
|||  
|-|-|  
|[AtlInternalQueryInterface](../vs140/AtlInternalQueryInterface.md)|Delegates to the                             **IUnknown** of a nonaggregated object.|  
|[InlineIsEqualIUnknown](../vs140/InlineIsEqualIUnknown.md)|Generates efficient code for comparing interfaces against                             **IUnknown**.|  
  
##  <a name="atlinternalqueryinterface"></a>  AtlInternalQueryInterface  
 Retrieves a pointer to the requested interface.  
  
```  
  
HRESULT  
AtlInternalQueryInterface(  
   void*  
pThis  
,  
   const _ATL_INTMAP_ENTRY*  
pEntries  
,  
   REFIID  
iid  
,  
   void**  
ppvObject  
);  
  
```  
  
### Parameters  
 `pThis`  
 [in] A pointer to the object that contains the COM map of interfaces exposed to                                 `QueryInterface`.  
  
 `pEntries`  
 [in] An array of                                 **_ATL_INTMAP_ENTRY** structures that access a map of available interfaces.  
  
 `iid`  
 [in] The GUID of the interface being requested.  
  
 `ppvObject`  
 [out] A pointer to the interface pointer specified in                                 `iid`, or                                 **NULL** if the interface is not found.  
  
### Return Value  
 One of the standard HRESULT values.  
  
### Remarks  
 `AtlInternalQueryInterface` only handles interfaces in the COM map table. If your object is aggregated,                         `AtlInternalQueryInterface` does not delegate to the outer unknown. You can enter interfaces into the COM map table with the macro                         [COM_INTERFACE_ENTRY](../vs140/COM_INTERFACE_ENTRY-Macros.md) or one of its variants.  
  
### Example  
 [!CODE [NVC_ATL_Windowing#94](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Windowing#94)]  
  
##  <a name="inlineisequaliunknown"></a>  InlineIsEqualIUnknown  
 Call this function, for the special case of testing for                 **IUnknown**.  
  
```  
  
BOOL InlineIsEqualUnknown(  
   REFGUID   
rguid1  
);  
  
```  
  
### Parameters  
 *rguid1*  
 [in] The GUID to compare to                                 **IID_IUnknown**.  
  
## See Also  
 [ATL Functions](../vs140/ATL-Functions.md)   
 [COM Map Macros](../vs140/COM-Map-Macros.md)