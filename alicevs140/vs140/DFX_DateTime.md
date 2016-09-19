---
title: "DFX_DateTime"
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
ms.assetid: 5f28ac10-9d30-4bdb-a540-215f017d1005
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DFX_DateTime
Transfers time and date data between the field data members of a [CDaoRecordset](../vs140/CDaoRecordset-Class.md) object and the columns of a record on the data source.  
  
## Syntax  
  
```  
  
      void AFXAPI DFX_DateTime(  
   CDaoFieldExchange* pFX,  
   LPCTSTR szName,  
   COleDateTime& value,  
   DWORD dwBindOptions = AFX_DAO_ENABLE_FIELD_CACHE   
);  
```  
  
#### Parameters  
 `pFX`  
 A pointer to an object of class [CDaoFieldExchange](../vs140/CDaoFieldExchange-Class.md). This object contains information to define the context for each call of the function.  
  
 `szName`  
 The name of a data column.  
  
 *value*  
 The value stored in the indicated data member — the value to be transferred. The function takes a reference to a [COleDateTime](../vs140/COleDateTime-Class.md) object. For a transfer from recordset to data source, this value is taken from the specified data member. For a transfer from data source to recordset, the value is stored in the specified data member.  
  
 `dwBindOptions`  
 An option that lets you take advantage of MFC's double buffering mechanism for detecting recordset fields that have changed. The default, `AFX_DAO_ENABLE_FIELD_CACHE`, uses double buffering. The other possible value is `AFX_DAO_DISABLE_FIELD_CACHE`. If you specify this value, MFC does no checking on this field. You must call `SetFieldDirty` and `SetFieldNull` yourself.  
  
> [!NOTE]
>  You can control whether data is double buffered by default by setting [CDaoRecordset::m_bCheckCacheForDirtyFields](../vs140/CDaoRecordset--m_bCheckCacheForDirtyFields.md).  
  
## Remarks  
 Data is mapped between type **DAO_DATE** in DAO and type [COleDateTime](../vs140/COleDateTime-Class.md) in the recordset.  
  
> [!NOTE]
>  `COleDateTime` replaces [CTime](../Topic/CTime%20Class.md) and **TIMESTAMP_STRUCT** for this purpose in the DAO classes. `CTime` and **TIMESTAMP_STRUCT** are still used for the ODBC-based data access classes.  
  
## Example  
 See [DFX_Text](../vs140/DFX_Text.md).  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DFX_Text](../vs140/DFX_Text.md)   
 [DFX_Bool](../vs140/DFX_Bool.md)   
 [DFX_Currency](../vs140/DFX_Currency.md)   
 [DFX_Long](../vs140/DFX_Long.md)   
 [DFX_Short](../vs140/DFX_Short.md)   
 [DFX_Single](../vs140/DFX_Single.md)   
 [DFX_Double](../vs140/DFX_Double.md)   
 [DFX_Byte](../vs140/DFX_Byte.md)   
 [DFX_Binary](../vs140/DFX_Binary.md)   
 [DFX_LongBinary](../vs140/DFX_LongBinary.md)   
 [CDaoFieldExchange::SetFieldType](../vs140/CDaoFieldExchange--SetFieldType.md)