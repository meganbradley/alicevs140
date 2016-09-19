---
title: "Supporting IDispatch and IErrorInfo"
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
ms.assetid: 7db2220f-319d-4ce9-9382-d340019f14f7
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Supporting IDispatch and IErrorInfo
You can use the template class [IDispatchImpl](../vs140/IDispatchImpl-Class.md) to provide a default implementation of the `IDispatch Interface` portion of any dual interfaces on your object.  
  
 If your object uses the `IErrorInfo` interface to report errors back to the client, then your object must support the `ISupportErrorInfo Interface` interface. The template class [ISupportErrorInfoImpl](../vs140/ISupportErrorInfoImpl-Class.md) provides an easy way to implement this if you only have a single interface that generates errors on your object.  
  
## See Also  
 [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md)