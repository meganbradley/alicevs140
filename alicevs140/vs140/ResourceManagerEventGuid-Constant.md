---
title: "ResourceManagerEventGuid Constant"
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
ms.topic: article
ms.assetid: b5d7a70b-0130-44d4-b03a-a1e9a789b8bd
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ResourceManagerEventGuid Constant
A category GUID describing ETW events fired by the Concurrency Runtime that are directly related to the resource manager.  
  
## Syntax  
  
```  
const __declspec(selectany) GUID ResourceManagerEventGuid = { 0x2718D25B, 0x5BF5, 0x4479, { 0x8E, 0x88, 0xBA, 0xBC, 0x64, 0xBD, 0xBF, 0xCA } };  
```  
  
## Remarks  
 This category of events is not currently fired by the Concurrency Runtime.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [concurrency Namespace](../vs140/concurrency-Namespace.md)   
 [IResourceManager Structure](../vs140/IResourceManager-Structure.md)