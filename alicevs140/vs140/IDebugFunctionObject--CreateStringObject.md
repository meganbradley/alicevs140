---
title: "IDebugFunctionObject::CreateStringObject"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fd6070ab-07d4-4ea1-8d71-b16592d6f1a7
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugFunctionObject::CreateStringObject
Creates a string object.  
  
## Syntax  
  
```cpp#  
HRESULT CreateStringObject(   
   LPCOLESTR      pcstrString,  
   IDebugObject** ppObject  
);  
```  
  
```c#  
int CreateStringObject(  
   string      pcstrString,   
   out IDebugObject ppOjbect  
);  
```  
  
#### Parameters  
 `pcstrString`  
 [in] The string value for the string object.  
  
 `ppObject`  
 [out] Returns an [IDebugObject](../vs140/IDebugObject.md) object that represents the newly created string object.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 Call this method to create an object that represents a string that is a parameter to the function which is represented by the [IDebugFunctionObject](../vs140/IDebugFunctionObject.md) interface.  
  
## See Also  
 [IDebugFunctionObject](../vs140/IDebugFunctionObject.md)