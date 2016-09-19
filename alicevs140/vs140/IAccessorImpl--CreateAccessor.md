---
title: "IAccessorImpl::CreateAccessor"
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
ms.assetid: f6b92075-c0b8-46ca-8361-026d562d24f5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAccessorImpl::CreateAccessor
Creates an accessor from a set of bindings.  
  
## Syntax  
  
```  
  
      STDMETHOD(CreateAccessor)(  
   DBACCESSORFLAGS dwAccessorFlags,  
   DBCOUNTITEM cBindings,  
   const DBBINDING rgBindings[],  
   DBLENGTH cbRowSize,  
   HACCESSOR* phAccessor,  
   DBBINDSTATUS rgStatus[]   
);  
```  
  
#### Parameters  
 See [IAccessor::CreateAccessor](https://msdn.microsoft.com/en-us/library/ms720969.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IAccessorImpl Class](../vs140/IAccessorImpl-Class.md)   
 [IAccessorImpl::AddRefAccessor](../vs140/IAccessorImpl--AddRefAccessor.md)   
 [IAccessorImpl::ReleaseAccessor](../vs140/IAccessorImpl--ReleaseAccessor.md)