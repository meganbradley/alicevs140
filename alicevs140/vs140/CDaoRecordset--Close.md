---
title: "CDaoRecordset::Close"
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
ms.assetid: 71ed9e01-9f23-4a80-b4dc-846ddaed7b56
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::Close
Closing a `CDaoRecordset` object removes it from the collection of open recordsets in the associated database.  
  
## Syntax  
  
```  
  
virtual void Close( );  
  
```  
  
## Remarks  
 Because **Close** does not destroy the `CDaoRecordset` object, you can reuse the object by calling **Open** on the same data source or a different data source.  
  
 All pending [AddNew](../vs140/CDaoRecordset--AddNew.md) or [Edit](../vs140/CDaoRecordset--Edit.md) statements are canceled, and all pending transactions are rolled back. If you want to preserve pending additions or edits, call [Update](../vs140/CDaoRecordset--Update.md) before you call **Close** for each recordset.  
  
 You can call **Open** again after calling **Close**. This lets you reuse the recordset object. A better alternative is to call [Requery](../vs140/CDaoRecordset--Requery.md), if possible.  
  
 For related information, see the topic "Close Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::Open](../vs140/CDaoRecordset--Open.md)   
 [CDaoRecordset::CDaoRecordset](../vs140/CDaoRecordset--CDaoRecordset.md)