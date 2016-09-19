---
title: "IDebugPropertyCreateEvent2::GetDebugProperty"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d7e43183-444c-4417-af19-82e28229f83a
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugPropertyCreateEvent2::GetDebugProperty
Gets the new property.  
  
## Syntax  
  
```cpp#  
HRESULT GetDebugProperty (   
   IDebugProperty2** ppProperty  
);  
```  
  
```c#  
int GetDebugProperty (   
   out IDebugProperty2 ppProperty  
);  
```  
  
#### Parameters  
 `ppProperty`  
 [out] Returns an [IDebugProperty2](../vs140/IDebugProperty2.md) object that represents the new property.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugPropertyCreateEvent2](../vs140/IDebugPropertyCreateEvent2.md)   
 [IDebugProperty2](../vs140/IDebugProperty2.md)