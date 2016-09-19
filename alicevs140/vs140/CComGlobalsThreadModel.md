---
title: "CComGlobalsThreadModel"
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
ms.assetid: f112382f-da0a-4bfe-bb49-80f9fd908d47
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComGlobalsThreadModel
Calls the appropriate thread model methods, regardless of the threading model being used.  
  
## Syntax  
  
```  
  
      #if defined( _ATL_SINGLE_THREADED )  
   typedef CComSingleThreadModel CComGlobalsThreadModel;  
#elif defined( _ATL_APARTMENT_THREADED )  
   typedef CComMultiThreadModel CComGlobalsThreadModel;  
#elif defined( _ATL_FREE_THREADED )  
   typedef CComMultiThreadModel CComGlobalsThreadModel;  
#else  
   #pragma message ("No global threading model defined")  
#endif  
```  
  
## Remarks  
 Depending on the threading model used by your application, the `typedef` name `CComGlobalsThreadModel` references either [CComSingleThreadModel](../vs140/CComSingleThreadModel-Class.md) or [CComMultiThreadModel](../vs140/CComMultiThreadModel-Class.md). These classes provide additional `typedef` names to reference a critical section class.  
  
> [!NOTE]
>  `CComGlobalsThreadModel` does not reference class [CComMultiThreadModelNoCS](../vs140/CComMultiThreadModelNoCS-Class.md).  
  
 Using `CComGlobalsThreadModel` frees you from specifying a particular threading model class. Regardless of the threading model being used, the appropriate methods will be called.  
  
 In addition to `CComGlobalsThreadModel`, ATL provides the `typedef` name [CComObjectThreadModel](../vs140/CComObjectThreadModel.md). The class referenced by each `typedef` depends on the threading model used, as shown in the following table:  
  
|typedef|Single threading|Apartment threading|Free threading|  
|-------------|----------------------|-------------------------|--------------------|  
|`CComObjectThreadModel`|S|S|M|  
|`CComGlobalsThreadModel`|S|M|M|  
  
 S=`CComSingleThreadModel`; M=`CComMultiThreadModel`  
  
 Use `CComObjectThreadModel` within a single object class. Use `CComGlobalsThreadModel` in an object that is globally available to your program, or when you want to protect module resources across multiple threads.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [Class Overview](../vs140/ATL-Class-Overview.md)   
 [Typedefs](../vs140/ATL-Typedefs.md)