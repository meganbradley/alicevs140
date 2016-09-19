---
title: "IDebugBinder3::GetMemoryObject"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71d959c7-45df-485f-b0ee-f1c0439d54fb
caps.latest.revision: 9
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugBinder3::GetMemoryObject
This method retrieves a memory object that represents the memory that this object is bound to.  
  
## Syntax  
  
```cpp  
HRESULT GetMemoryObject(  
   IDebugField*   pField,  
   UINT64         uConstant,  
   IDebugObject** ppObject  
);  
```  
  
```c#  
int GetMemoryObject(  
   IDebugField      pField,  
   long             uConstant,  
   out IDebugObject ppObject  
);  
```  
  
#### Parameters  
 `pField`  
 [in] Specifies which field to get the memory object for.  
  
 `uConstant`  
 [in] Represents a memory address or value for a constant value.  
  
 `ppObject`  
 [out] An [IDebugObject](../vs140/IDebugObject.md) representing the memory that this object is bound to.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise, returns an error code.  
  
## See Also  
 [IDebugBinder3](../vs140/IDebugBinder3.md)   
 [IDebugField](../vs140/IDebugField.md)   
 [IDebugObject](../vs140/IDebugObject.md)