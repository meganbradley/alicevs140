---
title: "id"
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
ms.assetid: a48d2c99-c5d2-4f46-bf96-5ac88dcb5d0c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# id
Specifies a `dispid` parameter for a member function (either a property or a method, in an interface or dispinterface).  
  
## Syntax  
  
```  
  
      [ id(  
   dispid  
) ]  
```  
  
#### Parameters  
 `dispid`  
 The dispatch ID for the interface method.  
  
## Remarks  
 The **id** C++ attribute has the same functionality as the [id](http://msdn.microsoft.com/library/windows/desktop/aa367040) MIDL attribute.  
  
## Example  
 See the example for [bindable](../vs140/bindable.md) for an example of how to use **id**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Interface method|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Method Attributes](../vs140/Method-Attributes.md)   
 [Data Member Attributes](../vs140/Data-Member-Attributes.md)   
 [defaultvalue](../vs140/defaultvalue.md)   
 [in](../vs140/in--C---.md)   
 [out](../vs140/out--C---.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)