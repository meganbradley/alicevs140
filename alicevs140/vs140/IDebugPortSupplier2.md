---
title: "IDebugPortSupplier2"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 37067324-2ea6-4a01-8829-a6e9c7a70068
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPortSupplier2
This interface supplies ports to the session debug manager (SDM).  
  
## Syntax  
  
```  
IDebugPortSupplier2 : IUnknown  
```  
  
## Notes for Implementers  
 A custom port supplier implements this interface to represent a port supplier.  
  
## Notes for Callers  
 A call to `CoCreateInstance` with a port supplier's `GUID` returns this interface (this is the typical way to obtain this interface). For example:  
  
```cpp#  
IDebugPortSupplier2 *GetPortSupplier(GUID *pPortSupplierGuid)  
{  
    IDebugPortSupplier2 *pPS = NULL;  
    if (pPortSupplierGuid != NULL) {  
        CComPtr<IDebugPortSupplier2> spPortSupplier;  
        spPortSupplier.CoCreateInstance(*pPortSupplierGuid);  
        if (spPortSupplier != NULL) {  
            pPS = spPortSupplier.Detach();  
        }  
    }  
    return (pPS);  
}  
```  
  
 A call to [IDebugCoreServer2::GetPortSupplier](../vs140/IDebugCoreServer2--GetPortSupplier.md) returns this interface, representing the current port supplier being used by [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)].  
  
 [IDebugPort2::GetPortSupplier](../vs140/IDebugPort2--GetPortSupplier.md) returns this interface, representing the port supplier that created the port.  
  
 [IEnumDebugPortSuppliers2](../vs140/IEnumDebugPortSuppliers2.md) represents a list of `IDebugPortSupplier` interfaces (the `IEnumDebugPortSuppliers` interface is obtained from [IDebugCoreServer2::EnumPortSuppliers](../vs140/IDebugCoreServer2--EnumPortSuppliers.md), representing all of the port suppliers registered with [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)]).  
  
 A debug engine typically does not interact with a port supplier.  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugPortSupplier2`.  
  
|Method|Description|  
|------------|-----------------|  
|[GetPortSupplierName](../vs140/IDebugPortSupplier2--GetPortSupplierName.md)|Gets the port supplier name.|  
|[GetPortSupplierId](../vs140/IDebugPortSupplier2--GetPortSupplierId.md)|Gets the port supplier identifier.|  
|[GetPort](../vs140/IDebugPortSupplier2--GetPort.md)|Gets a port from a port supplier.|  
|[EnumPorts](../vs140/IDebugPortSupplier2--EnumPorts.md)|Enumerates the ports that already exist.|  
|[CanAddPort](../vs140/IDebugPortSupplier2--CanAddPort.md)|Verifies that a port supplier supports adding new ports.|  
|[AddPort](../vs140/IDebugPortSupplier2--AddPort.md)|Adds a port.|  
|[RemovePort](../vs140/IDebugPortSupplier2--RemovePort.md)|Removes a port.|  
  
## Remarks  
 A port supplier can identify itself by name and ID, add and remove ports, and enumerate all ports that the port supplier provides.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../vs140/Core-Interfaces.md)   
 [IDebugPort2::GetPortSupplier](../vs140/IDebugPort2--GetPortSupplier.md)   
 [IDebugCoreServer2::GetPortSupplier](../vs140/IDebugCoreServer2--GetPortSupplier.md)   
 [IEnumDebugPortSuppliers2](../vs140/IEnumDebugPortSuppliers2.md)