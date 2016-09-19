---
title: "Updating Data with the ADO Data Control"
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
ms.assetid: 8bec34b9-93dd-4872-b023-55ac011ccff5
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Updating Data with the ADO Data Control
ADO data control data can be either read-only or modifiable.  
  
### To create an application that modifies data using ADO data control  
  
1.  Set ADO data control **CursorLocation** property. Options are:  
  
    -   Server Side  
  
    -   Client Side  
  
2.  Set ADO data control **LockType** property. The optimistic concurrency is recommended.  
  
3.  Set ADO data control **CursorType** property. Options are:  
  
    -   Keyset Cursor  
  
    -   Dynamic Cursor  
  
    -   Static Cursor  
  
     Make sure the OLE DB provider supports the chosen option.  
  
4.  Set the data-bound control's properties, as needed, to allow updateability. Note that some controls do not allow updating.  
  
 For more information about these properties, see the ADO documentation.  
  
## See Also  
 [ADO Databinding](../vs140/ADO-Databinding.md)   
 [Using ADO Databinding in Visual C++](../vs140/Using-ADO-Databinding-in-Visual-C--.md)