---
title: "CRowset::FindNextRow"
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
ms.assetid: 36484df9-3625-4f15-bf69-db73a8d91c55
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRowset::FindNextRow
Finds the next matching row after the specified bookmark.  
  
## Syntax  
  
```  
  
      HRESULT FindNextRow(   
   DBCOMPAREOP op,   
   BYTE* pData,   
   DBTYPE wType,   
   DBLENGTH nLength,   
   BYTE bPrecision,   
   BYTE bScale,   
   BOOL bSkipCurrent = TRUE,   
   CBookmarkBase* pBookmark = NULL    
) throw( );  
```  
  
#### Parameters  
 `op`  
 [in] The operation to use in comparing row values. For values, see [IRowsetFind::FindNextRow](https://msdn.microsoft.com/en-us/library/ms723091.aspx).  
  
 `pData`  
 [in] A pointer to the value to be matched.  
  
 `wType`  
 [in] Indicates the data type of the value part of the buffer. For information about type indicators, see [Data Types](https://msdn.microsoft.com/en-us/library/ms723969.aspx) in the *OLE DB Programmer's Reference* in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 `nLength`  
 [in] The length, in bytes, of the consumer data structure allocated for the data value. For details, see the description of **cbMaxLen** in [DBBINDING Structures](https://msdn.microsoft.com/en-us/library/ms716845.aspx) in the *OLE DB Programmer's Reference.*  
  
 `bPrecision`  
 [in] The maximum precision used when getting data. Used only if `wType` is `DBTYPE_NUMERIC`. For more information, see [Conversions involving DBTYPE_NUMERIC or DBTYPE_DECIMAL](https://msdn.microsoft.com/en-us/library/ms719714.aspx) in the *OLE DB Programmer's Reference*.  
  
 `bScale`  
 [in] The scale used when getting data. Used only if `wType` is `DBTYPE_NUMERIC` or **DBTYPE_DECIMAL**. For more information, see [Conversions involving DBTYPE_NUMERIC or DBTYPE_DECIMAL](https://msdn.microsoft.com/en-us/library/ms719714.aspx) in the *OLE DB Programmer's Reference*.  
  
 *bSkipCurrent*  
 [in] The number of rows from the bookmark at which to start a search.  
  
 `pBookmark`  
 [in] The bookmark for position at which to start a search.  
  
## Return Value  
 A standard `HRESULT`.  
  
## Remarks  
 This method requires the optional interface **IRowsetFind**, which might not be supported on all providers; if this is the case, the method returns **E_NOINTERFACE**. You must also set **DBPROP_IRowsetFind** to `VARIANT_TRUE` before calling **Open** on the table or command containing the rowset.  
  
 For information about using bookmarks in consumers, see [Using Bookmarks](../vs140/Using-Bookmarks.md).  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CRowset Class](../vs140/CRowset-Class.md)   
 [DBBINDING Structures](https://msdn.microsoft.com/en-us/library/ms716845.aspx)