---
title: "CAccessorBase::ReleaseAccessors"
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
ms.assetid: f08bc88e-0552-4a9c-9c65-b4061094649a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAccessorBase::ReleaseAccessors
Releases the accessors created by the class.  
  
## Syntax  
  
```  
  
      HRESULT ReleaseAccessors(  
   IUnknown* pUnk   
);  
```  
  
#### Parameters  
 *pUnk*  
 [in] A pointer to an **IUnknown** interface for the COM object for which the accessors have been created.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 Called from [CAccessorRowset::Close](../vs140/CAccessorRowset--Close.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CAccessorBase Class](../vs140/CAccessorBase-Class.md)