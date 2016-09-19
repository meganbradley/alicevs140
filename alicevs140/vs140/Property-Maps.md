---
title: "Property Maps"
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
ms.assetid: 44abde56-90ad-4612-854e-d2fa5426fa80
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property Maps
In addition to the session, rowset, and optional command object, each provider supports one or more properties. These properties are defined in property maps contained in the header files created by the OLE DB Provider Wizard. Each header file contains a map for the properties in the OLE DB property group defined for the object or objects defined in that file. The header file that contains the data source object also contains the property map for the [DataSource properties](https://msdn.microsoft.com/en-us/library/ms724188\(v=vs.140\).aspx). Session.h contains the property map for the [Session properties](https://msdn.microsoft.com/en-us/library/ms714221.aspx). The rowset and command objects reside in a single header file, called *projectname*RS.h. These properties are members of the [Rowset properties](https://msdn.microsoft.com/en-us/library/ms711252.aspx) group.  
  
## See Also  
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)