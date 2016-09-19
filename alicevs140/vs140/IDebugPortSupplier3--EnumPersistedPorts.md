---
title: "IDebugPortSupplier3::EnumPersistedPorts"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1c3dead3-5d6c-4067-8418-4015f0b0dd07
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortSupplier3::EnumPersistedPorts
This method retrieves an object that allows enumeration of the list of persisted ports.  
  
## Syntax  
  
```cpp  
HRESULT EnumPersistedPorts(  
   BSTR_ARRAY         PortNames,  
   IEnumDebugPorts2** ppEnum  
);  
```  
  
```c#  
int EnumPersistedPorts(  
   BSTR_ARRAY           PortNames,  
   out IEnumDebugPorts2 ppEnum  
);  
```  
  
#### Parameters  
 `PortNames`  
 [in] A [BSTR_ARRAY](../vs140/BSTR_ARRAY.md) structure that contains a list of port names to find and return among the persisted ports. Only those persisted ports with these names will be returned.  
  
 `ppEnum`  
 [out] An object that implements the [IEnumDebugPorts2](../vs140/IEnumDebugPorts2.md) interface.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Persisted ports are loaded when a port supplier is instantiated, and saved when the port supplier is destroyed.  
  
## See Also  
 [IDebugPortSupplier3](../vs140/IDebugPortSupplier3.md)   
 [IEnumDebugPorts2](../vs140/IEnumDebugPorts2.md)   
 [BSTR_ARRAY](../vs140/BSTR_ARRAY.md)