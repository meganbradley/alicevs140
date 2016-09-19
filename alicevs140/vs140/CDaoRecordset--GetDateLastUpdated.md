---
title: "CDaoRecordset::GetDateLastUpdated"
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
ms.assetid: d66c738a-e6e0-4eb2-a944-c8d9d2b2c489
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetDateLastUpdated
Call this member function to retrieve the date and time the schema was last updated.  
  
## Syntax  
  
```  
  
COleDateTime GetDateLastUpdated( );  
  
```  
  
## Return Value  
 A [COleDateTime](../vs140/COleDateTime-Class.md) object containing the date and time the base table structure (schema) was last updated.  
  
## Remarks  
 Date and time settings are derived from the computer on which the base table structure (schema) was last updated.  
  
 For related information, see the topic "DateCreated, LastUpdated Properties" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetDateCreated](../vs140/CDaoRecordset--GetDateCreated.md)