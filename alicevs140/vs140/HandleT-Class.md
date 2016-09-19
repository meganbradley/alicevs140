---
title: "HandleT Class"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 3822b32a-a426-4d94-a54d-919d4df60ee2
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HandleT Class
Represents a handle to an object.  
  
## Syntax  
  
```  
template <  
   typename HandleTraits  
>  
class HandleT;  
```  
  
#### Parameters  
 `HandleTraits`  
 An instance of the [HandleTraits](../vs140/HANDLETraits-Structure.md) stucture that defines common characteristics of a handle.  
  
## Members  
  
### Public Typedefs  
  
|Name|Description|  
|----------|-----------------|  
|`Traits`|A synonym for `HandleTraits`.|  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[HandleT::HandleT Constructor](../vs140/HandleT--HandleT-Constructor.md)|Initializes a new instance of the HandleT class.|  
|[HandleT::~HandleT Destructor](../vs140/HandleT--~HandleT-Destructor.md)|Deinitializes an instance of the HandleT class.|  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[HandleT::Attach Method](../vs140/HandleT--Attach-Method.md)|Associates the specified handle with the current HandleT object.|  
|[HandleT::Close Method](../vs140/HandleT--Close-Method.md)|Closes the current HandleT object.|  
|[HandleT::Detach Method](../vs140/HandleT--Detach-Method.md)|Disassociates the current HandleT object from its underlying handle.|  
|[HandleT::Get Method](../vs140/HandleT--Get-Method.md)|Gets the value of the underlying handle.|  
|[HandleT::IsValid Method](../vs140/HandleT--IsValid-Method.md)|Indicates whether the current HandleT object represents a handle.|  
  
### Protected Methods  
  
|Name|Description|  
|----------|-----------------|  
|[HandleT::InternalClose Method](../vs140/HandleT--InternalClose-Method.md)|Closes the current HandleT object.|  
  
### Public Operators  
  
|Name|Description|  
|----------|-----------------|  
|[HandleT::operator= Operator](../vs140/HandleT--operator=-Operator.md)|Moves the value of the specified HandleT object to the current HandleT object.|  
  
### Protected Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[HandleT::handle_ Data Member](../vs140/HandleT--handle_-Data-Member.md)|Contains the handle that is represented by the HandleT object.|  
  
## Inheritance Hierarchy  
 `HandleT`  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [Wrappers Namespace](../vs140/Microsoft--WRL--Wrappers-Namespace.md)