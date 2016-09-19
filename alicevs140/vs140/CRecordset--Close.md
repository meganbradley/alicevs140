---
title: "CRecordset::Close"
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
ms.assetid: 6534443b-8816-447d-ae36-76f11b6016ee
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::Close
Closes the recordset.  
  
## Syntax  
  
```  
  
virtual void Close( );  
```  
  
## Remarks  
 The ODBC **HSTMT** and all memory the framework allocated for the recordset are deallocated. Usually after calling **Close**, you delete the C++ recordset object if it was allocated with **new**.  
  
 You can call **Open** again after calling **Close**. This lets you reuse the recordset object. The alternative is to call **Requery**.  
  
## Example  
 [!CODE [NVC_MFCDatabase#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#17)]  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::CRecordset](../vs140/CRecordset--CRecordset.md)   
 [CRecordset::Open](../vs140/CRecordset--Open.md)   
 [CRecordset::Requery](../vs140/CRecordset--Requery.md)