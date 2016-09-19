---
title: "BEGIN_PROPSET_MAP"
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
ms.assetid: c3a30618-6025-4d49-8688-a171294d2e93
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BEGIN_PROPSET_MAP
Marks the beginning of the property set map entries.  
  
## Syntax  
  
```  
  
BEGIN_PROPSET_MAP(  
Class   
)  
  
```  
  
#### Parameters  
 *Class*  
 [in] The class in which this property set is specified. A property set can be specified in the following OLE DB objects:  
  
-   [Data Source Objects](https://msdn.microsoft.com/en-us/library/ms721278.aspx)  
  
-   [Session Objects](https://msdn.microsoft.com/en-us/library/ms711572.aspx)  
  
-   [Commands](https://msdn.microsoft.com/en-us/library/ms724608.aspx)  
  
## Example  
 Here is a sample property set map:  
  
 [!CODE [NVC_OLEDB_Provider#3](../CodeSnippet/VS_Snippets_Cpp/NVC_OLEDB_Provider#3)]  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [Macros for OLE DB Provider Templates](../vs140/Macros-for-OLE-DB-Provider-Templates.md)   
 [OLE DB Provider Templates](../vs140/OLE-DB-Provider-Templates--C---.md)   
 [OLE DB Provider Template Architecture](../vs140/OLE-DB-Provider-Template-Architecture.md)   
 [Creating an OLE DB Provider](../vs140/Creating-an-OLE-DB-Provider.md)