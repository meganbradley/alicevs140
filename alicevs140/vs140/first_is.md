---
title: "first_is"
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
ms.assetid: 89acbf56-3b38-4d44-83e8-1ce2f6f74ffd
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# first_is
Specifies the index of the first array element to be transmitted.  
  
## Syntax  
  
```  
  
      [ first_is(  
   "expression"  
) ]  
```  
  
#### Parameters  
 *expression*  
 One or more C-language expressions. Empty argument slots are allowed.  
  
## Remarks  
 The **first_is** C++ attribute has the same functionality as the [first_is](http://msdn.microsoft.com/library/windows/desktop/aa366831) MIDL attribute.  
  
## Example  
 The following code shows various ways to specify a section in an array:  
  
```  
// cpp_attr_ref_first_is.cpp  
// compile with: /LD  
#include "windows.h"  
#include "unknwn.h"  
  
[module(name="MyLib")];  
  
[object, uuid(11111111-1111-1111-1111-111111111111)]  
__interface b   
{  
   [id(0), propget, bindable, displaybind, defaultbind,   
requestedit] HRESULT get_I([out, retval]long *i);  
   HRESULT Proc1([in] short First, [in] short Last,   
[first_is(First), last_is(Last), size_is(Last-First)] char Arr1[]);   
   HRESULT Proc2([in] short First, [in] short Last,   
[last_is(First), size_is(Last)] char Arr2[]);  
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|Field in `struct` or **union**, interface parameter, interface method|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [Parameter Attributes](../vs140/Parameter-Attributes.md)   
 [last_is](../vs140/last_is.md)   
 [max_is](../vs140/max_is.md)   
 [length_is](../vs140/length_is.md)   
 [size_is](../vs140/size_is.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)