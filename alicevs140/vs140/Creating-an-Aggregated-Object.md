---
title: "Creating an Aggregated Object"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc29d7aa-fd53-4276-9c2f-37379f71b179
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Creating an Aggregated Object
Aggregation delegates **IUnknown** calls, providing a pointer to the outer object's **IUnknown** to the inner object.  
  
### To create an aggregated object  
  
1.  Add an **IUnknown** pointer to your class object and initialize it to **NULL** in the constructor.  
  
2.  Override [FinalConstruct](../vs140/CComObjectRootEx--FinalConstruct.md) to create the aggregate.  
  
3.  Use the **IUnknown** pointer, defined in Step 1, as the second parameter for the [COM_INTERFACE_ENTRY_AGGREGATE](../vs140/COM_INTERFACE_ENTRY_AGGREGATE.md) macros.  
  
4.  Override [FinalRelease](../vs140/CComObjectRootEx--FinalRelease.md) to release the **IUnknown** pointer.  
  
> [!NOTE]
>  If you use and release an interface from the aggregated object during `FinalConstruct`, you should add the [DECLARE_PROTECT_FINAL_CONSTRUCT](../vs140/DECLARE_PROTECT_FINAL_CONSTRUCT.md) macro to the definition of your class object.  
  
## See Also  
 [Fundamentals of ATL COM Objects](../vs140/Fundamentals-of-ATL-COM-Objects.md)