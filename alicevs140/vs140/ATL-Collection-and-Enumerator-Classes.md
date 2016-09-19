---
title: "ATL Collection and Enumerator Classes"
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
ms.assetid: 6818db73-7094-48d8-a0ca-18147beec362
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Collection and Enumerator Classes
ATL provides the following classes to help you implement collections and enumerators.  
  
|Class|Description|  
|-----------|-----------------|  
|[ICollectionOnSTLImpl](../vs140/ICollectionOnSTLImpl-Class.md)|Collection interface implementation|  
|[IEnumOnSTLImpl](../vs140/IEnumOnSTLImpl-Class.md)|Enumerator interface implementation (assumes data stored in an STL-compatible container)|  
|[CComEnumImpl](../vs140/CComEnumImpl-Class.md)|Enumerator interface implementation (assumes data stored in an array)|  
|[CComEnumOnSTL](../vs140/CComEnumOnSTL-Class.md)|Enumerator object implementation (uses `IEnumOnSTLImpl`)|  
|[CComEnum](../vs140/CComEnum-Class.md)|Enumerator object implementation (uses `CComEnumImpl`)|  
|[_Copy](../vs140/ATL-Copy-Policy-Classes.md)|Copy policy class|  
|[_CopyInterface](../vs140/ATL-Copy-Policy-Classes.md)|Copy policy class|  
|[CAdapt](../vs140/CAdapt-Class.md)|Adapter class (hides **operator &** allowing `CComPtr`, `CComQIPtr`, and `CComBSTR` to be stored in STL containers)|  
  
## See Also  
 [Collections and Enumerators](../vs140/ATL-Collections-and-Enumerators.md)