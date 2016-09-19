---
title: "default (C++)"
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
ms.assetid: 0cdca716-1ba8-46d7-9399-167e55492870
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# default (C++)
Indicates that the custom or dispinterface defined within a coclass represents the default programmability interface.  
  
## Syntax  
  
```  
  
      [ default(  
   interface1,  
   interface2  
) ]  
```  
  
#### Parameters  
 *interface1*  
 The default interface that will be made available to scripting environments that create an object based on the class defined with the **default** attribute.  
  
 If no default interface is specified, the first occurrence of a nonsource interface is used as the default.  
  
 *interface2*(optional)  
 The default source interface. You must also specify this interface with the [source](../vs140/source--C---.md) attribute.  
  
 If no default source interface is specified, the first source interface is used as the default.  
  
## Remarks  
 The **default** C++ attribute has the same functionality as the [default](http://msdn.microsoft.com/library/windows/desktop/aa366787) MIDL attribute. The **default** attribute is also used with the [case](../vs140/case--C---.md) attribute.  
  
## Example  
 The following code shows how **default** is used on the definition of a coclass to specify **ICustomDispatch** as the default programmability interface:  
  
```  
// cpp_attr_ref_default.cpp  
// compile with: /LD  
#include "windows.h"  
[module(name="MyLibrary")];  
  
[object, uuid("9E66A290-4365-11D2-A997-00C04FA37DDB")]  
__interface ICustom {  
   HRESULT Custom([in] long l, [out, retval] long *pLong);  
};  
  
[dual, uuid("9E66A291-4365-11D2-A997-00C04FA37DDB")]   
__interface IDual {  
   HRESULT Dual([in] long l, [out, retval] long *pLong);  
};  
  
[object, uuid("9E66A293-4365-11D2-A997-00C04FA37DDB")]  
__interface ICustomDispatch : public IDispatch {  
   HRESULT Dispatch([in] long l, [out, retval] long *pLong);  
};  
  
[   coclass,  
   default(ICustomDispatch),   
   source(IDual),  
   uuid("9E66A294-4365-11D2-A997-00C04FA37DDB")  
]  
class CClass : public ICustom, public IDual, public ICustomDispatch {  
   HRESULT Custom(long l, long *pLong) { return(S_OK); }  
   HRESULT Dual(long l, long *pLong) { return(S_OK); }  
   HRESULT Dispatch(long l, long *pLong) { return(S_OK); }  
};  
  
int main() {  
#if 0 // Can't instantiate without implementations of IUnknown/IDispatch  
   CClass *pClass = new CClass;  
  
   long llong;  
  
   pClass->custom(1, &llong);  
   pClass->dual(1, &llong);  
   pClass->dispinterface(1, &llong);  
   pClass->dispatch(1, &llong);  
  
   delete pClass;  
#endif  
   return(0);  
}  
```  
  
 The [source](../vs140/source--C---.md) attribute also has an example of how to use **default**.  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**, `struct`, data member|  
|**Repeatable**|No|  
|**Required attributes**|**coclass** (when applied to **class** or `struct`)|  
|**Invalid attributes**|None|  
  
 For more information, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [coclass](../vs140/coclass.md)   
 [Attributes Samples](assetId:///558ebdb2-082f-44dc-b442-d8d33bf7bdb8)