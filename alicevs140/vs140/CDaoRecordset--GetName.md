---
title: "CDaoRecordset::GetName"
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
ms.assetid: e7cd5330-512f-4c9f-9e27-ebd459ddf83e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetName
Call this member function to retrieve the name of the recordset.  
  
## Syntax  
  
```  
  
CString GetName( );  
  
```  
  
## Return Value  
 A `CString` containing the name of the recordset.  
  
## Remarks  
 The name of the recordset must start with a letter and can contain a maximum of 40 characters. It can include numbers and underscore characters but can't include punctuation or spaces.  
  
 For related information, see the topic "Name Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetDefaultDBName](../vs140/CDaoRecordset--GetDefaultDBName.md)   
 [CDaoRecordset::GetDefaultSQL](../vs140/CDaoRecordset--GetDefaultSQL.md)   
 [CDaoRecordset::GetSQL](../vs140/CDaoRecordset--GetSQL.md)   
 [CDaoRecordset::GetType](../vs140/CDaoRecordset--GetType.md)