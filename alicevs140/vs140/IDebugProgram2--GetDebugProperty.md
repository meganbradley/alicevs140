---
title: "IDebugProgram2::GetDebugProperty"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d194224e-f0e6-46ab-85d4-9e2639e28946
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugProgram2::GetDebugProperty
Gets the program's properties.  
  
## Syntax  
  
```cpp#  
HRESULT GetDebugProperty(   
   IDebugProperty2** ppProperty  
);  
```  
  
```c#  
int GetDebugProperty(   
   out IDebugProperty2 ppProperty  
);  
```  
  
#### Parameters  
 `ppProperty`  
 [out] Returns an [IDebugProperty2](../vs140/IDebugProperty2.md) object that represents the program's properties.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## Remarks  
 The properties returned by this method are specific to the program. If the program needs to return more than one property, then the [IDebugProperty2](../vs140/IDebugProperty2.md) object returned by this method is a container of additional properties and calling the [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md) method returns a list of all properties.  
  
 A program may expose any number and type of additional properties that can be described through the `IDebugProperty2` interface. An IDE might display the additional program properties through a generic property browser user interface.  
  
## See Also  
 [IDebugProgram2](../vs140/IDebugProgram2.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)   
 [IDebugProperty2::EnumChildren](../vs140/IDebugProperty2--EnumChildren.md)