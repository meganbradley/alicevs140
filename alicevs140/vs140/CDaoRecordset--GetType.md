---
title: "CDaoRecordset::GetType"
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
ms.assetid: 3d4c9db2-d0be-4af3-9909-f4bd13fbcbd7
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetType
Call this member function after opening the recordset to determine the type of the recordset object.  
  
## Syntax  
  
```  
  
short GetType( );  
  
```  
  
## Return Value  
 One of the following values that indicates the type of a recordset:  
  
-   **dbOpenTable** Table-type recordset  
  
-   **dbOpenDynaset** Dynaset-type recordset  
  
-   **dbOpenSnapshot** Snapshot-type recordset  
  
## Remarks  
 For related information, see the topic "Type Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetDefaultDBName](../vs140/CDaoRecordset--GetDefaultDBName.md)   
 [CDaoRecordset::GetDefaultSQL](../vs140/CDaoRecordset--GetDefaultSQL.md)   
 [CDaoRecordset::GetName](../vs140/CDaoRecordset--GetName.md)   
 [CDaoRecordset::GetSQL](../vs140/CDaoRecordset--GetSQL.md)