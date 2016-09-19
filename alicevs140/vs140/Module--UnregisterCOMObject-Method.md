---
title: "Module::UnregisterCOMObject Method"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 5d377525-0385-482a-a215-6e8a1f032861
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Module::UnregisterCOMObject Method
Unregisters one or more COM objects, which prevents other applications from connecting to them.  
  
## Syntax  
  
```  
virtual HRESULT UnregisterCOMObject(  
   const wchar_t* serverName,  
   DWORD* cookies,  
   unsigned int count  
```  
  
#### Parameters  
 `serverName`  
 (Unused)  
  
 `cookies`  
 An array of pointers to values that identify the class objects to be unregistered. The array was created by the [RegisterCOMObject](../vs140/Module--RegisterCOMObject-Method.md) method.  
  
 `count`  
 The number of classes to unregister.  
  
## Return Value  
 S_OK if this operation is successful; otherwise, an error HRESULT that indicates the reason the operation failed.  
  
## Requirements  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## See Also  
 [Module Class](../vs140/Module-Class.md)