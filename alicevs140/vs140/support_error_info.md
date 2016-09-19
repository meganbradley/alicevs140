---
title: "support_error_info"
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
ms.assetid: 20a2b55c-4738-4b35-a71d-e5e9c3a7e3bc
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# support_error_info
Implements support for returning detailed errors.  
  
## Syntax  
  
```  
  
      [ support_error_info(  
   error_interface=uuid  
) ]  
```  
  
#### Parameters  
 **error_interface**  
 The identifier of the interface implementing **IErrorInfo**.  
  
## Remarks  
 The **support_error_info** C++ attribute implements support for returning detailed, contextual errors encountered by the target object to the client. For the object to support errors, the methods of the **IErrorInfo** interface must be implemented by the object. For more information, see [Supporting IDispatch and IErrorInfo](../vs140/Supporting-IDispatch-and-IErrorInfo.md).  
  
 This attribute adds the [ISupportErrorInfoImpl](../vs140/ISupportErrorInfoImpl-Class.md) class as a base class to the target object. This results in a default implementation of **ISupportErrorInfo** and can be used when a single interface generates errors on an object.  
  
## Example  
 The following code adds default support for the **ISupportErrorInfo** interface to the `CMyClass` object.  
  
```  
// cpp_attr_ref_support_error_info.cpp  
// compile with: /LD  
#define _ATL_ATTRIBUTES  
#include "atlbase.h"  
#include "atlcom.h"  
  
[module (name="mymod")];  
[object, uuid("f0b17d66-dc6e-4662-baaf-76758e09c878")]  
__interface IMyErrors  
{  
};  
  
[ coclass, support_error_info("IMyErrors"),  
  uuid("854dd392-bdc7-4781-8667-8757936f2a4f") ]  
class CMyClass  
{  
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**|  
|**Repeatable**|Yes|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [COM Attributes](../vs140/COM-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)