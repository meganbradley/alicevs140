---
title: "IPropertyProxyProvider::GetPropertyProxy"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3ebb7515-5bfe-48f4-9b8d-721b8f664eb6
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IPropertyProxyProvider::GetPropertyProxy
Retrieves the property proxy interface for the specified proxy ID.  
  
## Syntax  
  
```cpp#  
HRESULT GetPropertyProxy(  
   DWORD                  dwID,  
   IPropertyProxyEESide** proxy  
);  
```  
  
```c#  
int GetPropertyProxy(  
   uint                     dwID,  
   out IPropertyProxyEESide proxy  
);  
```  
  
#### Parameters  
 `dwID`  
 [in] ID of the desired property proxy.  
  
 `proxy`  
 [out] Returns an [IPropertyProxyEESide](../vs140/IPropertyProxyEESide.md) object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 To support external type visualizers, this method typically forwards the call to the [IEEVisualizerService::GetPropertyProxy](../vs140/IEEVisualizerService--GetPropertyProxy.md) method. See [Visualizing and Viewing Data](../vs140/Visualizing-and-Viewing-Data.md) for details on how the IEEVisualizerService is obtained.  
  
## See Also  
 [IPropertyProxyProvider](../vs140/IPropertyProxyProvider.md)   
 [IPropertyProxyEESide](../vs140/IPropertyProxyEESide.md)   
 [IEEVisualizerService::GetPropertyProxy](../vs140/IEEVisualizerService--GetPropertyProxy.md)   
 [Visualizing and Viewing Data](../vs140/Visualizing-and-Viewing-Data.md)