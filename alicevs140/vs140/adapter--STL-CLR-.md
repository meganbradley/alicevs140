---
title: "adapter (STL-CLR)"
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
H1: adapter (STL/CLR)
ms.assetid: 71ce7e51-42b6-4f70-9595-303791a97677
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# adapter (STL-CLR)
The STL/CLR header `<cliext/adapter>` specifies two template classes (`collection_adapter` and `range_adapter`), and the template function `make_collection`.  
  
## Syntax  
  
```  
#include <cliext/adapter>  
```  
  
## Remarks  
  
|Class|Description|  
|-----------|-----------------|  
|[collection_adapter](../vs140/collection_adapter--STL-CLR-.md)|Wraps the Base Class Library (BCL) collection as a range.|  
|[range_adapter](../vs140/range_adapter--STL-CLR-.md)|Wraps the range as a BCL collection.|  
  
|Function|Description|  
|--------------|-----------------|  
|[make_collection](../vs140/make_collection--STL-CLR-.md)|Creates a range adapter using an iterator pair.|  
  
## Requirements  
 **Header:** <cliext/adapter>  
  
 **Namespace:** cliext  
  
## See Also  
 [STL/CLR Library Reference](../vs140/STL-CLR-Library-Reference.md)