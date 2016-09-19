---
title: "call_as"
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
ms.assetid: a09d7f1f-353b-4870-9b45-f0284161695d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# call_as
Enables a [local](../vs140/local--C---.md) function to be mapped to a remote function so that when the remote function is called, the local function is invoked.  
  
## Syntax  
  
```  
  
      [ call_as(  
   function  
) ]  
```  
  
#### Parameters  
 *function*  
 The local function that you want to be called when a remote function is invoked.  
  
## Remarks  
 The **call_as** C++ attribute has the same functionality as the [call_as](http://msdn.microsoft.com/library/windows/desktop/aa366748) MIDL attribute.  
  
## Example  
 The following code shows how you can use **call_as** to map a nonremotable function (**f1**) to a remotable function (**Remf1**):  
  
```  
// cpp_attr_ref_call_as.cpp  
// compile with: /LD  
#include "unknwn.h"  
[module(name="MyLib")];  
[dual, uuid("00000000-0000-0000-0000-000000000001")]  
__interface IMInterface {  
   [local] HRESULT f1 ( int i );  
   [call_as(f1)] HRESULT Remf1 ( int i );   
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Interface method|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Method Attributes](../vs140/Method-Attributes.md)   
 [local](../vs140/local--C---.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)