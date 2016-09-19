---
title: "RoInitializeWrapper Class"
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
ms.assetid: 4055fbe0-63a7-4c06-b5a0-414fda5640e5
caps.latest.revision: 4
translation.priority.ht: 
  - de-de
  - ja-jp
---
# RoInitializeWrapper Class
Initializes the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)].  
  
## Syntax  
  
```  
class RoInitializeWrapper  
```  
  
## Remarks  
 RoInitializeWrapper is a convenience that initializes the [!INCLUDE[wrt](../vs140/includes/wrt_md.md)] and returns an HRESULT that indicates whether the operation was successful.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[RoInitializeWrapper::RoInitializeWrapper](../vs140/RoInitializeWrapper--RoInitializeWrapper-Constructor.md)|Initializes a new instance of the RoInitializeWrapper class.|  
|[RoInitializeWrapper::~RoInitializeWrapper](../vs140/RoInitializeWrapper--~RoInitializeWrapper-Destructor.md)|Destroys the current instance of the RoInitializeWrapper class.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[HRESULT()](../vs140/RoInitializeWrapper--HRESULT---Operator.md)|Retrieves the HRESULT produced by the RoInitializeWrapper constructor.|  
  
## Inheritance Hierarchy  
 `RoInitializeWrapper`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Wrappers Namespace](../vs140/Microsoft--WRL--Wrappers-Namespace.md)