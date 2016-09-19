---
title: "IAccessorImpl::AddRefAccessor"
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
ms.assetid: 4c15392c-944b-4cbd-8cc7-2a5c2f308a70
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAccessorImpl::AddRefAccessor
Adds a reference count to an existing accessor.  
  
## Syntax  
  
```  
  
      STDMETHOD(AddRefAccessor)(  
   HACCESSOR hAccessor,  
   DBREFCOUNT* pcRefCount   
);  
```  
  
#### Parameters  
 See [IAccessor::AddRefAccessor](https://msdn.microsoft.com/en-us/library/ms714978.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [IAccessorImpl Class](../vs140/IAccessorImpl-Class.md)   
 [IAccessorImpl::CreateAccessor](../vs140/IAccessorImpl--CreateAccessor.md)   
 [IAccessorImpl::ReleaseAccessor](../vs140/IAccessorImpl--ReleaseAccessor.md)