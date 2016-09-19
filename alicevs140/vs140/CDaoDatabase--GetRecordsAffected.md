---
title: "CDaoDatabase::GetRecordsAffected"
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
ms.assetid: b688843e-1634-4257-87cb-f118ef6cd136
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoDatabase::GetRecordsAffected
Call this member function to determine the number of records affected by the most recent call of the [Execute](../vs140/CDaoDatabase--Execute.md) member function.  
  
## Syntax  
  
```  
  
long GetRecordsAffected( );  
  
```  
  
## Return Value  
 A long integer containing the number of records affected.  
  
## Remarks  
 The value returned includes the number of records deleted, updated, or inserted by an action query run with **Execute**. The count returned will not reflect changes in related tables when cascade updates or deletes are in effect.  
  
 For related information, see the topic "RecordsAffected Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoDatabase Class](../vs140/CDaoDatabase-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)