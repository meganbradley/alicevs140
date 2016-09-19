---
title: "IDebugFunctionObject::CreateArrayObject"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a380e53c-15f1-401f-927f-f366eea789e6
caps.latest.revision: 12
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugFunctionObject::CreateArrayObject
Creates an array object. This array can contain either primitive or object instance values.  
  
## Syntax  
  
```cpp#  
HRESULT CreateArrayObject(   
   OBJECT_TYPE    ot,  
   IDebugField*   pClassField,  
   DWORD          dwRank,  
   DWORD          dwDims[],  
   DWORD          dwLowBounds[],  
   IDebugObject** ppObject  
);  
```  
  
```c#  
int CreateArrayObject(  
   enum_OBJECT_TYPE ot,   
   IDebugField      pClassField,   
   uint             dwRank,   
   uint[]           dwDims,   
   uint[]           dwLowBounds,   
   out IDebugObject ppObject  
);  
```  
  
#### Parameters  
 `ot`  
 [in] Specifies a value from the [OBJECT_TYPE](../vs140/OBJECT_TYPE.md) enumeration indicating the type of the new array object.  
  
 `pClassField`  
 [in] An [IDebugField](../vs140/IDebugField.md) object representing the class of an object, if creating an array of object instance values. If creating an array of primitive objects, this parameter is a null value.  
  
 `dwRank`  
 [in] The rank or number of dimensions of the array.  
  
 `dwDims`  
 [in] The sizes of each dimension of the array.  
  
 `dwLowBounds`  
 [in] The origin of each dimension (typically 0 or 1).  
  
 `ppObject`  
 [out] Returns an [IDebugObject](../vs140/IDebugObject.md) object representing the newly created array. This is actually an [IDebugArrayObject](../vs140/IDebugArrayObject.md) object.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 Call this method to create an object that represents an array parameter to the function which is represented by the [IDebugFunctionObject](../vs140/IDebugFunctionObject.md) interface.  
  
## See Also  
 [IDebugFunctionObject](../vs140/IDebugFunctionObject.md)