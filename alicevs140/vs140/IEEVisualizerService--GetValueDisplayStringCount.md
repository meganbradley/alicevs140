---
title: "IEEVisualizerService::GetValueDisplayStringCount"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d683a833-fbfb-4042-84df-6905124a268a
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IEEVisualizerService::GetValueDisplayStringCount
Retrieves the number of value strings to display for the specified property or field.  
  
## Syntax  
  
```cpp#  
HRESULT GetValueDisplayStringCount (  
   DWORD         displayKind,   
   IDebugField * propertyOrField,   
   ULONG *       pcelt  
);  
```  
  
```c#  
int GetValueDisplayStringCount (  
   uint        displayKind,   
   IDebugField propertyOrField,   
   out ulong   pcelt  
);  
```  
  
#### Parameters  
 `displayKind`  
 [in] Value from the [DisplayKind](../vs140/DisplayKind.md) enumeration.  
  
 `propertyOrField`  
 [in] An [IDebugField](../vs140/IDebugField.md) interface that represents a property or field.  
  
 `pcelt`  
 [out] Returns the number of value strings to display.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IEEVisualizerService](../vs140/IEEVisualizerService.md)