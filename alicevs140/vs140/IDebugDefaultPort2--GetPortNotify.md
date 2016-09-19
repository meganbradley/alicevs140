---
title: "IDebugDefaultPort2::GetPortNotify"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3ae715ee-9886-4694-a52b-59bb3b27467a
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugDefaultPort2::GetPortNotify
This method gets an [IDebugPortNotify2](../vs140/IDebugPortNotify2.md) interface for this port.  
  
## Syntax  
  
```cpp  
HRESULT GetPortNotify(  
   IDebugPortNotify2** ppPortNotify  
);  
```  
  
```c#  
int GetPortNotify(  
   out IDebugPortNotify2 ppPortNotify  
);  
```  
  
#### Parameters  
 `ppPortNotify`  
 [out] An [IDebugPortNotify2](../vs140/IDebugPortNotify2.md) object.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 Normally, the `QueryInterface` method is called on the object implementing the [IDebugPort2](../vs140/IDebugPort2.md) interface to obtain an [IDebugPortNotify2](../vs140/IDebugPortNotify2.md) interface. However, there are circumstances in which the desired interface is implemented on a different object. This method hides those circumstances and returns the `IDebugPortNotify2` interface from the most appropriate object.  
  
## See Also  
 [IDebugDefaultPort2](../vs140/IDebugDefaultPort2.md)   
 [IDebugPortNotify2](../vs140/IDebugPortNotify2.md)