---
title: "Data Source Object Interfaces"
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
ms.assetid: 929e100c-c08c-4b64-8437-d8d1357226f6
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Data Source Object Interfaces
The following table shows the mandatory and optional interfaces defined by OLE DB for a data source object.  
  
|Interface|Required?|Implemented by OLE DB templates?|  
|---------------|---------------|--------------------------------------|  
|`IDBCreateSession`|Mandatory|Yes|  
|`IDBInitialize`|Mandatory|Yes|  
|`IDBProperties`|Mandatory|Yes|  
|[IPersist](http://msdn.microsoft.com/library/windows/desktop/ms688695)|Mandatory|Yes|  
|[IConnectionPointContainer](http://msdn.microsoft.com/library/windows/desktop/ms683857)|Optional|No|  
|`IDBDataSourceAdmin`|Optional|No|  
|`IDBInfo`|Optional|No|  
|[IPersistFile](http://msdn.microsoft.com/library/windows/desktop/ms687223)|Optional|No|  
|`ISupportErrorInfo`|Optional|No|  
  
 The data source object implements the `IDBProperties`, `IDBInitialize`, and `IDBCreateSession` interfaces through inheritance. You can choose to support additional functionality by inheriting or not inheriting from one of these implementation classes. If you want to support the `IDBDataSourceAdmin` interface, you must inherit from the `IDBDataSourceAdminImpl` class.  
  
## See Also  
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)