---
title: "BEGIN_PROPERTY_SET_EX"
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
ms.assetid: c95e7fab-edce-47b8-b282-200e53a2ea8a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_PROPERTY_SET_EX
Marks the beginning of a property set in a property set map.  
  
## Syntax  
  
```  
  
BEGIN_PROPERTY_SET_EX(  
guid  
, flags )  
```  
  
#### Parameters  
 `guid`  
 [in] The property GUID.  
  
 `flags`  
 [in] **UPROPSET_HIDDEN** for any property sets you do not wish to expose, or **UPROPSET_PASSTHROUGH** for a provider exposing properties defined outside the scope of the provider.  
  
## Example  
 See [BEGIN_PROPSET_MAP](../vs140/BEGIN_PROPSET_MAP.md).  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [Macros for OLE DB Provider Templates](../vs140/Macros-for-OLE-DB-Provider-Templates.md)   
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)   
 [Creating an OLE DB Provider](../vs140/Creating-an-OLE-DB-Provider.md)