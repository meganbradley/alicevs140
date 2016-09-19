---
title: "CDaoTableDef::CreateField"
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
ms.assetid: 8b23f89c-25c9-4bb7-92ed-6de3e4ac9f95
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::CreateField
Call this member function to add a field to the table.  
  
## Syntax  
  
```  
  
      void CreateField(   
   LPCTSTR lpszName,   
   short nType,   
   long lSize,   
   long lAttributes = 0    
);  
void CreateField(   
   CDaoFieldInfo& fieldinfo    
);  
```  
  
#### Parameters  
 `lpszName`  
 A pointer to a string expression specifying the name of this field.  
  
 `nType`  
 A value indicating the data type of the field. The setting can be one of these values:  
  
|Type|Size (bytes)|Description|  
|----------|--------------------|-----------------|  
|**dbBoolean**|1 byte|BOOL|  
|**dbByte**|1|BYTE|  
|**dbInteger**|2|int|  
|**dbLong**|4|long|  
|**dbCurrency**|8|Currency ([COleCurrency](../vs140/COleCurrency-Class.md))|  
|**dbSingle**|4|float|  
|**dbDouble**|8|double|  
|**dbDate**|8|Date/Time ([COleDateTime](../vs140/COleDateTime-Class.md))|  
|**dbText**|1 – 255|Text ([CString](../vs140/CStringT-Class.md))|  
|**dbLongBinary**|0|Long Binary (OLE Object), [CLongBinary](../vs140/CLongBinary-Class.md) or [CByteArray](../vs140/CByteArray-Class.md)|  
|**dbMemo**|0|Memo ([CString](../vs140/CStringT-Class.md))|  
  
 `lSize`  
 A value that indicates the maximum size, in bytes, of a field that contains text, or the fixed size of a field that contains text or numeric values. The `lSize` parameter is ignored for all but text fields.  
  
 `lAttributes`  
 A value corresponding to characteristics of the field and that can be combined using a bitwise-OR.  
  
|Constant|Description|  
|--------------|-----------------|  
|**dbFixedField**|The field size is fixed (default for Numeric fields).|  
|**dbVariableField**|The field size is variable (Text fields only).|  
|**dbAutoIncrField**|The field value for new records is automatically incremented to a unique long integer that cannot be changed. Only supported for Microsoft Jet database tables.|  
|**dbUpdatableField**|The field value can be changed.|  
|**dbDescending**|The field is sorted in descending (Z – A or 100 – 0) order (applies only to a Field object in a Fields collection of an Index object). If you omit this constant, the field is sorted in ascending (A – Z or 0 – 100) order (default).|  
  
 `fieldinfo`  
 A reference to a [CDaoFieldInfo](../vs140/CDaoFieldInfo-Structure.md) structure.  
  
## Remarks  
 A **DAOField** (OLE) object is created and appended to the Fields collection of the **DAOTableDef** (OLE) object. Besides its use for examining object properties, you can also use `CDaoFieldInfo` to construct an input parameter for creating new fields in a tabledef. The first version of `CreateField` is simpler to use, but if you want finer control, you can use the second version of `CreateField`, which takes a `CDaoFieldInfo` parameter.  
  
 If you use the version of `CreateField` that takes a `CDaoFieldInfo` parameter, you must carefully set each of the following members of the `CDaoFieldInfo` structure:  
  
-   **m_strName**  
  
-   `m_nType`  
  
-   **m_lSize**  
  
-   **m_lAttributes**  
  
-   **m_bAllowZeroLength**  
  
 The remaining members of `CDaoFieldInfo` should be set to **0**, **FALSE**, or an empty string, as appropriate for the member, or a `CDaoException` may occur.  
  
 For related information, see the topic "CreateField Method" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::DeleteField](../vs140/CDaoTableDef--DeleteField.md)   
 [CDaoTableDef::CreateIndex](../vs140/CDaoTableDef--CreateIndex.md)   
 [CDaoTableDef::DeleteIndex](../vs140/CDaoTableDef--DeleteIndex.md)