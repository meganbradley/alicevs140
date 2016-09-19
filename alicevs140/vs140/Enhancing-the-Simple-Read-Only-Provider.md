---
title: "Enhancing the Simple Read-Only Provider"
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
ms.assetid: cba0e09f-44c1-41c1-9456-332aa13dc158
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Enhancing the Simple Read-Only Provider
This section shows how to enhance the [simple read-only provider](../vs140/Implementing-the-Simple-Read-Only-Provider.md) created in the previous section. `IRowsetLocateImpl` creates an implementation for the `IRowsetLocate` interface and adds bookmark support for you.  
  
 When you have a working provider, you might want to enhance it to make the provider update, handle transactions, or enhance the performance of the row-fetching algorithm. Most provider enhancements involve adding an interface to an existing COM object.  
  
 The example in the following topics enhances the row-fetching mechanism by adding the `IRowsetLocate` interface to `CAgentRowset`. The topics show you how to:  
  
-   [Make RMyProviderRowset inherit from IRowsetLocate](../vs140/Modifying-the-Inheritance-of-RMyProviderRowset.md).  
  
-   [Dynamically determine the columns returned to the consumer](../vs140/Dynamically-Determining-Columns-Returned-to-the-Consumer.md).  
  
## See Also  
 [Creating a Simple Read-Only Provider](../vs140/Creating-a-Simple-Read-Only-Provider.md)