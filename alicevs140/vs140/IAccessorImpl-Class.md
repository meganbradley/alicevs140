---
title: "IAccessorImpl Class"
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
ms.assetid: 768606da-8b71-417c-a62c-88069ce7730d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAccessorImpl Class
Provides an implementation of the [IAccessor](https://msdn.microsoft.com/en-us/library/ms719672.aspx) interface.  
  
## Syntax  
  
```  
template <  
   class T,   
   class BindType = ATLBINDINGS,   
   class BindingVector = CAtlMap <   
      HACCESSOR hAccessor,   
      BindType* pBindingsStructure   
   >   
>  
class ATL_NO_VTABLE IAccessorImpl : public IAccessorImplBase<BindType>  
```  
  
#### Parameters  
 `T`  
 Your rowset or command object class.  
  
 `BindType`  
 Storage unit for binding information. The default is the **ATLBINDINGS** structure (see atldb.h).  
  
 `BindingVector`  
 Storage unit for column information. The default is [CAtlMap](../vs140/CAtlMap-Class.md) where the key element is an **HACCESSOR** value and the value element is a pointer to a `BindType` structure.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[IAccessorImpl](../vs140/IAccessorImpl-Class.md)|The constructor.|  
  
### Interface Methods  
  
|||  
|-|-|  
|[AddRefAccessor](../vs140/IAccessorImpl--AddRefAccessor.md)|Adds a reference count to an existing accessor.|  
|[CreateAccessor](../vs140/IAccessorImpl--CreateAccessor.md)|Creates an accessor from a set of bindings.|  
|[GetBindings](../vs140/IAccessorImpl--GetBindings.md)|Returns the bindings in an accessor.|  
|[ReleaseAccessor](../vs140/IAccessorImpl--ReleaseAccessor.md)|Releases an accessor.|  
  
## Remarks  
 This is mandatory on rowsets and commands. OLE DB requires providers to implement an **HACCESSOR**, which is a tag to an array of [DBBINDING](https://msdn.microsoft.com/en-us/library/ms716845.aspx) structures. **HACCESSOR**s provided by `IAccessorImpl` are addresses of the `BindType` structures. By default, `BindType` is defined as an **ATLBINDINGS** in `IAccessorImpl`'s template definition. `BindType` provides a mechanism used by `IAccessorImpl` to track the number of elements in its **DBBINDING** array as well as a reference count and accessor flags.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)