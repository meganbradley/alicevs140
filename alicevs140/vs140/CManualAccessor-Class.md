---
title: "CManualAccessor Class"
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
ms.assetid: a0088074-7135-465c-b228-69097a50b8cc
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CManualAccessor Class
Represents an accessor type designed for advanced use.  
  
## Syntax  
  
```  
class CManualAccessor : public CAccessorBase  
```  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[AddBindEntry](../vs140/CManualAccessor--AddBindEntry.md)|Adds a bind entry to the output columns.|  
|[AddParameterEntry](../vs140/CManualAccessor--AddParameterEntry.md)|Adds a parameter entry to the parameter accessor.|  
|[CreateAccessor](../vs140/CManualAccessor--CreateAccessor.md)|Allocates memory for the column bind structures and initializes the column data members.|  
|[CreateParameterAccessor](../vs140/CManualAccessor--CreateParameterAccessor.md)|Allocates memory for the parameter bind structures and initializes the parameter data members.|  
  
## Remarks  
 Using `CManualAccessor`, you can specify the parameter and output column binding by run-time function calls.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [DBViewer](../vs140/Visual-C---Samples.md)   
 [OLE DB Consumer Templates](../vs140/OLE-DB-Consumer-Templates--C---.md)   
 [Consumer Architecture Chart](../vs140/OLE-DB-Consumer-Templates-Reference.md)   
 [CAccessor Class](../vs140/CAccessor-Class.md)   
 [CDynamicAccessor Class](../vs140/CDynamicAccessor-Class.md)   
 [CDynamicParameterAccessor Class](../vs140/CDynamicParameterAccessor-Class.md)