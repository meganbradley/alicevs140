---
title: "CComObjectRoot Class"
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
ms.topic: reference
ms.assetid: f8797c38-6e73-4f67-85c2-71654cffa8eb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRoot Class
This typedef of [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md) is templatized on the default threading model of the server.  
  
## Syntax  
  
```  
  
typedef CComObjectRootEx<CComObjectThreadModel> CComObjectRoot;  
  
```  
  
## Remarks  
 `CComObjectRoot` is a `typedef` of [CComObjectRootEx](../vs140/CComObjectRootEx-Class.md) templatized on the default threading model of the server. Thus [CComObjectThreadModel](../vs140/CComObjectThreadModel.md) will reference either [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) or [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md).  
  
 `CComObjectRootEx` handles object reference count management for both nonaggregated and aggregated objects. It holds the object reference count if your object is not being aggregated, and holds the pointer to the outer unknown if your object is being aggregated. For aggregated objects, `CComObjectRootEx` methods can be used to handle the failure of the inner object to construct, and to protect the outer object from deletion when inner interfaces are released or the inner object is deleted.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class Members](assetId:///e3ce9c3d-9c8e-4fe5-b682-8e56740a0164)   
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComAggObject Class](../vs140/CComAggObject-Class.md)   
 [CComObject Class](../vs140/CComObject-Class.md)   
 [CComPolyObject Class](../vs140/CComPolyObject-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)