---
title: "coclass"
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
ms.assetid: 42da6a10-3af9-4b43-9a1d-689d00b61eb3
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# coclass
Creates a COM object, which can implement a COM interface.  
  
## Syntax  
  
```  
  
[coclass]  
  
```  
  
## Remarks  
 The **coclass** C++ attribute places a coclass construct in the generated .idl file.  
  
 When defining a coclass, you can also specify the [uuid](../vs140/uuid--C---Attributes-.md), [version](../vs140/version--C---.md), [threading](../vs140/threading--C---.md), [vi_progid](../vs140/vi_progid.md), and [progid](../vs140/progid.md) attributes. If any one of them is not specified, it will be generated.  
  
 If two header files contain classes with the **coclass** attribute and don't specify a GUID, the compiler will use the same GUID for both classes, and that will result in a MIDL error.  Therefore, you should use the `uuid` attribute when you use **coclass**.  
  
 **ATL Projects**  
  
 When this attribute precedes a class or structure definition in an ATL project, it:  
  
-   Injects code or data to support auto registration for the object.  
  
-   Injects code or data to support a COM class factory for the object.  
  
-   Injects code or data to implement **IUnknown** and make the object a COM-creatable object.  
  
 Specifically, the following base classes are added to the target object:  
  
-   [CComCoClass Class](../vs140/CComCoClass-Class.md) provides the default class factory and aggregation model for the object.  
  
-   [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md) has a template based on the threading model class specified by the [threading](../vs140/threading--C---.md) attribute. If the **threading** attribute is not specified, the default threading model is apartment.  
  
-   [IProvideClassInfo2Impl](../vs140/IProvideClassInfo2Impl-Class.md) is added if the [noncreatable](../vs140/noncreatable.md) attribute is not specified for the target object.  
  
 Finally, any dual interface that is not defined using embedded IDL is replaced with the corresponding [IDispatchImpl](../vs140/IDispatchImpl-Class.md) class. If the dual interface is defined in embedded IDL, the particular interface in the base list is not modified.  
  
 The **coclass** attribute also makes the following functions available via injected code, or in the case of `GetObjectCLSID`, as a static method in the base class `CComCoClass`:  
  
-   `UpdateRegistry` registers the class factories of the target class.  
  
-   `GetObjectCLSID`, which is related to registration, can also be used to obtain the CLSID of the target class.  
  
-   **GetObjectFriendlyName** by default returns a string of the format "<*target class name*> `Object`". If this function is already present, it is not added. Add this function to the target class to return a friendlier name than the one automatically generated.  
  
-   **GetProgID**, which is related to registration, returns the string specified with the [progid](../vs140/progid.md) attribute.  
  
-   **GetVersionIndependentProgID** has the same functionality as **GetProgID**, but it returns the string specified with [vi_progid](../vs140/vi_progid.md).  
  
 The following changes, which are related to the COM map, are made to the target class:  
  
-   A COM map is added with entries for all interfaces the target class derives from and all entries specified by the [COM Interface Entry Points](../vs140/COM-Interface-Entry-Points.md) attribute or those required by the [aggregates](../vs140/aggregates.md) attribute.  
  
-   An [OBJECT_ENTRY_AUTO](../vs140/OBJECT_ENTRY_AUTO.md) macro is inserted into the COM map. This macro is similar to [OBJECT_ENTRY](assetId:///abd10ee2-54f0-4f94-9ec2-ddf8f4c8c8cd) in terms of functionality but does not need to be part of the COM map of the target class.  
  
 The name of the coclass generated in the .idl file for the class will have the same name as the class.  For example, and referring to the following sample, to access the class ID for a coclass CMyClass, in a client through the MIDL-generated header file, use CLSID_CMyClass.  
  
## Example  
 The following code shows how to use the **coclass** attribute:  
  
```  
// cpp_attr_ref_coclass1.cpp  
// compile with: /LD  
#include "unknwn.h"  
[module(name="MyLib")];  
  
[ object, uuid("00000000-0000-0000-0000-000000000001") ]  
__interface I {  
   HRESULT func();  
};  
  
[coclass, progid("MyCoClass.coclass.1"), vi_progid("MyCoClass.coclass"),   
appobject, uuid("9E66A294-4365-11D2-A997-00C04FA37DDB")]  
class CMyClass : public I {};  
```  
  
 The following sample shows how to override the default implementation of a function that appears in the code injected by the **coclass** attribute. See [/Fx](../vs140/-Fx--Merge-Injected-Code-.md) for more information on viewing injected code. Any base classes or interfaces that you use for a class will be appear in the injected code.   Further, if a class is included by default in the injected code and you explicitly specify that class as a base for your coclass, the attribute provider will use the form specified in your code.  
  
```  
// cpp_attr_ref_coclass2.cpp  
// compile with: /LD  
#include <atlbase.h>  
#include <atlcom.h>  
#include <atlwin.h>  
#include <atltypes.h>  
#include <atlctl.h>  
#include <atlhost.h>  
#include <atlplus.h>  
  
[module(name="MyLib")];  
  
[object, uuid("00000000-0000-0000-0000-000000000000")]  
__interface bb {};  
  
[coclass, uuid("00000000-0000-0000-0000-000000000001")]  
class CMyClass : public bb {  
public:  
   // by adding the definition of UpdateRegistry to your code,   
   // the function will not be included in the injected code  
   static HRESULT WINAPI UpdateRegistry(BOOL bRegister) {  
      // you can add to the default implementation  
      CRegistryVirtualMachine rvm;  
      HRESULT hr;  
      if (FAILED(hr = rvm.AddStandardReplacements()))  
         return hr;  
      rvm.AddReplacement(_T("FriendlyName"), GetObjectFriendlyName());  
      return rvm.VMUpdateRegistry(GetOpCodes(), GetOpcodeStringVals(),  
         GetOpcodeDWORDVals(), GetOpcodeBinaryVals(), bRegister);  
   }  
};  
```  
  
## Requirements  
  
### Attribute Context  
  
|||  
|-|-|  
|**Applies to**|**class**, `struct`|  
|**Repeatable**|No|  
|**Required attributes**|None|  
|**Invalid attributes**|None|  
  
 For more information about the attribute contexts, see [Attribute Contexts](../vs140/Attribute-Contexts.md).  
  
## See Also  
 [IDL Attributes](../vs140/IDL-Attributes.md)   
 [COM Attributes](../vs140/COM-Attributes.md)   
 [Class Attributes](../vs140/Class-Attributes.md)   
 [Typedef, Enum, Union, and Struct Attributes](../vs140/Typedef--Enum--Union--and-Struct-Attributes.md)   
 [appobject](../vs140/appobject.md)