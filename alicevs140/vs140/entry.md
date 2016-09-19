---
title: "entry"
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
ms.assetid: ba4843e3-d7ad-4b86-9a15-0b4192f0f698
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# entry
Specifies an exported function or constant in a module by identifying the entry point in the DLL.  
  
## Syntax  
  
```  
  
      [ entry(  
   id  
) ]  
```  
  
#### Parameters  
 `id`  
 The ID of the entry point.  
  
## Remarks  
 The **entry** C++ attribute has the same functionality as the [entry](http://msdn.microsoft.com/library/windows/desktop/aa366815) MIDL attribute.  
  
## Example  
 See the example for [idl_module](../vs140/idl_module.md) for an example use of **entry**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|`idl_module` attribute|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)