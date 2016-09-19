---
title: "CDaoRecordset::GetDateCreated"
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
ms.assetid: a34d5f9a-19e7-4360-9df1-7462f0dc68e7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetDateCreated
Call this member function to retrieve the date and time a base table was created.  
  
## Syntax  
  
```  
  
COleDateTime GetDateCreated( );  
  
```  
  
## Return Value  
 A [COleDateTime](../vs140/COleDateTime-Class.md) object containing the date and time the base table was created.  
  
## Remarks  
 Date and time settings are derived from the computer on which the base table was created.  
  
 For related information, see the topic "DateCreated, LastUpdated Properties" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetDateLastUpdated](../vs140/CDaoRecordset--GetDateLastUpdated.md)