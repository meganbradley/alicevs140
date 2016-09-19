---
title: "source (C++)"
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
ms.assetid: 1878d05d-7709-4e97-b114-c62f38f5140e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# source (C++)
On a class, specifies the COM object's source interfaces for connection points. On a property or method, indicates that the member returns an object or VARIANT that is a source of events.  
  
## Syntax  
  
```  
  
      [ source(  
   interfaces  
) ]  
```  
  
#### Parameters  
 `interfaces`  
 One or more interfaces that you specify when you apply the source attribute to a class. This parameter is not used when source is applied to a property or method.  
  
## Remarks  
 The **source** C++ attribute has the same functionality as the [source](http://msdn.microsoft.com/library/windows/desktop/aa367166) MIDL attribute.  
  
 You can use the [default](../vs140/default--C---.md) attribute to specify the default source interface for an object.  
  
## Example  
  
```  
// cpp_attr_ref_source.cpp  
// compile with: /LD  
#include "windows.h"  
#include "unknwn.h"  
[module(name="MyLib")];  
  
[object, uuid(11111111-1111-1111-1111-111111111111)]  
__interface b  
{  
   [id(0), propget, bindable, displaybind, defaultbind, requestedit]  
   HRESULT get_I([out, retval]long *i);  
};  
  
[object, uuid(11111111-1111-1111-1111-111111111131)]  
__interface c  
{  
   [id(0), propget, bindable, displaybind, defaultbind, requestedit]   
   HRESULT et_I([out, retval]long *i);  
};  
  
[coclass, default(c), uuid(11111111-1111-1111-1111-111111111132)]  
class N : public b  
{  
};  
  
[coclass, source(c), default(b, c), uuid(11111111-1111-1111-1111-111111111133)]  
class NN : public b  
{  
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**, `struct`, `interface`|  
|**Repeatable**|No|  
|**Required attributes**|**coclass** (when applied to class or struct)|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [Method Attributes](../vs140/Method-Attributes.md)   
 [coclass](../vs140/coclass.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)