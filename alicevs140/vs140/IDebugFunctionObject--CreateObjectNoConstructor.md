---
title: "IDebugFunctionObject::CreateObjectNoConstructor"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4e2bd6d5-f4bd-4c10-a998-3db451c9a0c8
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugFunctionObject::CreateObjectNoConstructor
Creates an object with no constructor.  
  
## Syntax  
  
```cpp#  
HRESULT CreateObjectNoConstructor(   
   IDebugField*   pClassObject,  
   IDebugObject** ppObject  
);  
```  
  
```c#  
int CreateObjectNoConstructor(  
   IDebugField      pClassField,   
   out IDebugObject ppObject  
);  
```  
  
#### Parameters  
 `pClassObject`  
 [in] An [IDebugField](../vs140/IDebugField.md) object representing the type of the object to be created.  
  
 `ppObject`  
 [out] Returns an [IDebugObject](../vs140/IDebugObject.md) representing the newly created object.  
  
## Return Value  
 If successful, returns S_OK; otherwise, returns an error code.  
  
## Remarks  
 Call this method to create an object that represents an instance of a structure or complex type (that does not require a constructor) that is a parameter to the function which is represented by the [IDebugFunctionObject](../vs140/IDebugFunctionObject.md) interface.  
  
 If the object parameter requires a constructor, call the [CreateObject](../vs140/IDebugFunctionObject--CreateObject.md) method.  
  
## See Also  
 [IDebugField](../vs140/IDebugField.md)   
 [IDebugFunctionObject](../vs140/IDebugFunctionObject.md)   
 [CreateObject](../vs140/IDebugFunctionObject--CreateObject.md)