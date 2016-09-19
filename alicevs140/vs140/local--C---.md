---
title: "local (C++)"
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
ms.topic: language-reference
ms.assetid: 35cdd668-bd8e-492a-b7b8-263e7b662437
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# local (C++)
When used in the interface header, allows you to use the MIDL compiler as a header generator. When used in an individual function, designates a local procedure for which no stubs are generated.  
  
## Syntax  
  
```  
  
[local]  
  
```  
  
## Remarks  
 The `local` C++ attribute has the same functionality as the [local](http://msdn.microsoft.com/library/windows/desktop/aa367071) MIDL attribute.  
  
## Example  
 See [call_as](../vs140/call_as.md) for an example of how to use `local`.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|`interface`, interface method|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|**dispinterface**|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Interface Attributes](../vs140/Interface-Attributes.md)   
 [Method Attributes](../vs140/Method-Attributes.md)   
 [call_as](../vs140/call_as.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)