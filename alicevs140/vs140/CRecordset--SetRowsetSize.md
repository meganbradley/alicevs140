---
title: "CRecordset::SetRowsetSize"
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
ms.assetid: 3133662e-2196-4b2c-a775-b0708a6bf480
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::SetRowsetSize
Specifies the number of records you wish to retrieve during a fetch.  
  
## Syntax  
  
```  
  
      virtual void SetRowsetSize(  
   DWORD dwNewRowsetSize   
);  
```  
  
#### Parameters  
 *dwNewRowsetSize*  
 The number of rows to retrieve during a given fetch.  
  
## Remarks  
 This virtual member function specifies how many rows you wish to retrieve during a single fetch when using bulk row fetching. To implement bulk row fetching, you must set the `CRecordset::useMultiRowFetch` option in the `dwOptions` parameter of the [Open](../vs140/CRecordset--Open.md) member function.  
  
> [!NOTE]
>  Calling `SetRowsetSize` without implementing bulk row fetching will result in a failed assertion.  
  
 Call `SetRowsetSize` before calling **Open** to initially set the rowset size for the recordset. The default rowset size when implementing bulk row fetching is 25.  
  
> [!NOTE]
>  Use caution when calling `SetRowsetSize`. If you are manually allocating storage for the data (as specified by the **CRecordset::userAllocMultiRowBuffers** option of the dwOptions parameter in **Open**), you should check whether you need to reallocate these storage buffers after you call `SetRowsetSize`, but before you perform any cursor navigation operation.  
  
 To obtain the current setting for the rowset size, call [GetRowsetSize](../vs140/CRecordset--GetRowsetSize.md).  
  
 For more information about bulk row fetching, see the article [Recordset: Fetching Records in Bulk (ODBC)](../vs140/Recordset--Fetching-Records-in-Bulk--ODBC-.md).  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Open](../vs140/CRecordset--Open.md)   
 [CRecordset::GetRowsetSize](../vs140/CRecordset--GetRowsetSize.md)   
 [CRecordset::CheckRowsetError](../vs140/CRecordset--CheckRowsetError.md)   
 [CRecordset::DoBulkFieldExchange](../vs140/CRecordset--DoBulkFieldExchange.md)