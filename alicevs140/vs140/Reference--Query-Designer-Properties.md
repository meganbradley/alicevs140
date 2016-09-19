---
title: "Reference: Query Designer Properties"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - lightswitch
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dcfbc0ee-2cd3-4e5c-acd3-41f91d47fc28
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Reference: Query Designer Properties
You can modify the appearance and behavior of a query by setting the value of properties in the **Properties** window. The following tables describe each property.  
  
## General  
  
|Name|Description|  
|----------|-----------------|  
|**Number of Results Returned**|Indicates whether the query returns one row or multiple rows. Select one of the following values:<br /><br /> -   **Many** if you intend for this query to return a collection of rows (For example: a collection of customers).<br />-   **One** if you intend for this query to return only one row (For example: a customer). If no data matches the conditions of the query, the query returns `null` or `Nothing` in Visual Basic. If more than one row of data matches the conditions of the query, an `InvalidOperationException` is thrown.|  
|**Name**|The name of the query.|  
|**Is Optional**|Indicates whether a parameter value is required or optional. Select one of the following values:<br /><br /> -   `True` if you want the query to exclude filter conditions that use the parameter when the value of the parameter is null.<br />-   `False` if you want the query to include filter conditions that use the parameter when the value of the parameter is null. Each row of data will be tested for the presence of a null value.<br /><br /> Applies to query parameters only.|  
|**Source**|The data source of the query (For example: the `Customers` entity set).|  
|**Return Type**|The entity that the query returns when the query is executed.|  
  
## Appearance  
  
|Name|Description|  
|----------|-----------------|  
|**Description**|The text that appears as a tooltip.|  
|**Display Name**|The name that appears on the screen.|  
  
## See Also  
 [Reference: Screen Designer Properties](../vs140/Reference--Screen-Designer-Properties.md)   
 [Reference: Data Designer Properties](../vs140/Reference--Data-Designer-Properties.md)   
 [Queries: Retrieving Information from a Data Source](../Topic/Queries:%20Retrieving%20Information%20from%20a%20Data%20Source.md)