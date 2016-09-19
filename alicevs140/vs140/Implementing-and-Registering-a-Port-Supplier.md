---
title: "Implementing and Registering a Port Supplier"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fb057052-ee16-4272-8e16-a4da5dda0ad4
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Implementing and Registering a Port Supplier
The role of a port supplier is to track and supply ports, which in turn manage processes. At the time a port needs to be created, the port supplier is instantiated using CoCreate with the port supplier's GUID (the session debug manager [SDM] will use the port supplier the user selected or the port supplier specified by the project system). The SDM will then call [CanAddPort](../vs140/IDebugPortSupplier2--CanAddPort.md) to see if any ports can be added. If a port can be added, a new port is requested by calling [AddPort](../vs140/IDebugPortSupplier2--AddPort.md) and passing it an [IDebugPortRequest2](../vs140/IDebugPortRequest2.md) that describes the port. `AddPort` will return a new port represented by an [IDebugPort2](../vs140/IDebugPort2.md) interface.  
  
## Discussion  
 A port is created by a port supplier, which is in turn associated with a machine or debug server. A server can enumerate its port suppliers through the[EnumPortSuppliers](../vs140/IDebugCoreServer2--EnumPortSuppliers.md) method, and a port supplier can enumerate its ports through the [EnumPorts](../vs140/IDebugPortSupplier2--EnumPorts.md) method.  
  
 In addition to the typical COM registration, a port supplier must register itself with Visual Studio by placing its CLSID and name in specific registry locations. A Debugging SDK helper function called `SetMetric` handles this chore: it is called once for each item to be registered, thus:  
  
```cpp#  
SetMetric(metrictypePortSupplier,  
          <GUID of your port supplier>,  
          metricCLSID,  
          <CLSID of your port supplier>,  
          false,  
          NULL)  
SetMetric(metrictypePortSupplier,  
          <GUID of your port supplier>,  
          metricName,  
          <name of your port supplier>,  
          false,  
          NULL);  
```  
  
 A port supplier unregisters itself by calling `RemoveMetric` (another Debugging SDK helper function) once for each item that was registered, thus:  
  
```cpp#  
RemoveMetric(metrictypePortSupplier,  
             <GUID of your port supplier>,  
             metricCLSID,  
             NULL);  
RemoveMetric(metrictypePortSupplier,  
             <GUID of your port supplier>,  
             metricName,  
             NULL);  
```  
  
> [!NOTE]
>  The [Debugging SDK Helpers](../vs140/SDK-Helpers-for-Debugging.md)`SetMetric` and `RemoveMetric` are static functions defined in dbgmetric.h and compiled into ad2de.lib. The `metrictypePortSupplier`, `metricCLSID`, and `metricName` helpers are also defined in dbgmetric.h.  
  
 A port supplier can supply its name and GUID through the methods [GetPortSupplierName](../vs140/IDebugPortSupplier2--GetPortSupplierName.md) and [GetPortSupplierId](../vs140/IDebugPortSupplier2--GetPortSupplierId.md), respectively.  
  
## See Also  
 [Implementing a Port Supplier](../vs140/Implementing-a-Port-Supplier.md)   
 [Debugging SDK Helpers](../vs140/SDK-Helpers-for-Debugging.md)   
 [Port Suppliers](../vs140/Port-Suppliers.md)