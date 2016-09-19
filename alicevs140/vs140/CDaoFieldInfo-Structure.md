---
title: "CDaoFieldInfo Structure"
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
ms.assetid: 91b13e3f-bdb8-440c-86fc-ba4181ea0182
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoFieldInfo Structure
The `CDaoFieldInfo` structure contains information about a field object defined for data access objects (DAO).  
  
## Syntax  
  
```  
  
      struct CDaoFieldInfo  
{  
   CString m_strName;           // Primary  
   short m_nType;               // Primary  
   long m_lSize;                // Primary  
   long m_lAttributes;          // Primary  
   short m_nOrdinalPosition;    // Secondary  
   BOOL m_bRequired;            // Secondary  
   BOOL m_bAllowZeroLength;     // Secondary  
   long m_lCollatingOrder;      // Secondary  
   CString m_strForeignName;    // Secondary  
   CString m_strSourceField;    // Secondary  
   CString m_strSourceTable;    // Secondary  
   CString m_strValidationRule; // All  
   CString m_strValidationText; // All  
   CString m_strDefaultValue;   // All  
};  
```  
  
#### Parameters  
 `m_strName`  
 Uniquely names the field object. For details, see the topic "Name Property" in DAO Help.  
  
 `m_nType`  
 A value that indicates the data type of the field. For details, see the topic "Type Property" in DAO Help. The value of this property can be one of the following:  
  
-   **dbBoolean** Yes/No, same as **TRUE**/**FALSE**  
  
-   **dbByte** Byte  
  
-   **dbInteger** Short  
  
-   **dbLong** Long  
  
-   **dbCurrency** Currency; see MFC class [COleCurrency](../vs140/COleCurrency-Class.md)  
  
-   **dbSingle** Single  
  
-   **dbDouble** Double  
  
-   **dbDate** Date/Time; see MFC class [COleDateTime](../vs140/COleDateTime-Class.md)  
  
-   **dbText** Text; see MFC class [CString](../vs140/CStringT-Class.md)  
  
-   **dbLongBinary** Long Binary (OLE Object); you might want to use MFC class [CByteArray](../vs140/CByteArray-Class.md) instead of class `CLongBinary` as `CByteArray` is richer and easier to use.  
  
-   **dbMemo** Memo; see MFC class `CString`  
  
-   **dbGUID** A Globally Unique Identifier/Universally Unique Identifier used with remote procedure calls. For more information, see the topic "Type Property" in DAO Help.  
  
> [!NOTE]
>  Do not use string data types for binary data. This causes your data to pass through the Unicode/ANSI translation layer, resulting in increased overhead and possibly unexpected translation.  
  
 *m_lSize*  
 A value that indicates the maximum size, in bytes, of a DAO field object that contains text or the fixed size of a field object that contains text or numeric values. For details, see the topic "Size Property" in DAO Help. Sizes can be one of the following values:  
  
|Type|Size (Bytes)|Description|  
|----------|--------------------|-----------------|  
|**dbBoolean**|1 byte|Yes/No (same as True/False)|  
|**dbByte**|1|Byte|  
|**dbInteger**|2|Integer|  
|**dbLong**|4|Long|  
|**dbCurrency**|8|Currency ([COleCurrency](../vs140/COleCurrency-Class.md))|  
|**dbSingle**|4|Single|  
|**dbDouble**|8|Double|  
|**dbDate**|8|Date/Time ([COleDateTime](../vs140/COleDateTime-Class.md))|  
|**dbText**|1 - 255|Text ([CString](../vs140/CStringT-Class.md))|  
|**dbLongBinary**|0|Long Binary (OLE Object; [CByteArray](../vs140/CByteArray-Class.md); use instead of `CLongBinary`)|  
|**dbMemo**|0|Memo ([CString](../vs140/CStringT-Class.md))|  
|**dbGUID**|16|A Globally Unique Identifier/Universally Unique Identifier used with remote procedure calls.|  
  
 `m_lAttributes`  
 Specifies characteristics of a field object contained by a tabledef, recordset, querydef, or index object. The value returned can be a sum of these constants, created with the C++ bitwise-OR (**&#124;**) operator:  
  
-   **dbFixedField** The field size is fixed (default for Numeric fields).  
  
-   **dbVariableField** The field size is variable (Text fields only).  
  
-   **dbAutoIncrField** The field value for new records is automatically incremented to a unique long integer that cannot be changed. Only supported for Microsoft Jet database tables.  
  
-   **dbUpdatableField** The field value can be changed.  
  
-   **dbDescending** The field is sorted in descending (Z - A or 100 - 0) order (applies only to a field object in a Fields collection of an index object; in MFC, index objects are themselves contained in tabledef objects). If you omit this constant, the field is sorted in ascending (A - Z or 0 - 100) order (default).  
  
 When checking the setting of this property, you can use the C++ bitwise-AND operator (**&**) to test for a specific attribute. When setting multiple attributes, you can combine them by combining the appropriate constants with the bitwise-OR (**&#124;**) operator. For details, see the topic "Attributes Property" in DAO Help.  
  
 *m_nOrdinalPosition*  
 A value that specifies the numeric order in which you want a field represented by a DAO field object to be displayed relative to other fields. You can set this property with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md). For details, see the topic "OrdinalPosition Property" in DAO Help.  
  
 `m_bRequired`  
 Indicates whether a DAO field object requires a non-Null value. If this property is **TRUE**, the field does not allow a Null value. If Required is set to **FALSE**, the field can contain Null values as well as values that meet the conditions specified by the AllowZeroLength and ValidationRule property settings. For details, see the topic "Required Property" in DAO Help. You can set this property for a tabledef with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md).  
  
 *m_bAllowZeroLength*  
 Indicates whether an empty string ("") is a valid value of a DAO field object with a Text or Memo data type. If this property is **TRUE**, an empty string is a valid value. You can set this property to **FALSE** to ensure that you cannot use an empty string to set the value of a field. For details, see the topic "AllowZeroLength Property" in DAO Help. You can set this property for a tabledef with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md).  
  
 `m_lCollatingOrder`  
 Specifies the sequence of the sort order in text for string comparison or sorting. For details, see the topic "Customizing Windows Registry Settings for Data Access" in DAO Help. For a list of the possible values returned, see the **m_lCollatingOrder** member of the [CDaoDatabaseInfo](../vs140/CDaoDatabaseInfo-Structure.md) structure. You can set this property for a tabledef with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md).  
  
 `m_strForeignName`  
 A value that, in a relation, specifies the name of the DAO field object in a foreign table that corresponds to a field in a primary table. For details, see the topic "ForeignName Property" in DAO Help.  
  
 *m_strSourceField*  
 Indicates the name of the field that is the original source of the data for a DAO field object contained by a tabledef, recordset, or querydef object. This property indicates the original field name associated with a field object. For example, you could use this property to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table. For details, see the topic "SourceField, SourceTable Properties" in DAO Help. You can set this property for a tabledef with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md).  
  
 *m_strSourceTable*  
 Indicates the name of the table that is the original source of the data for a DAO field object contained by a tabledef, recordset, or querydef object. This property indicates the original table name associated with a field object. For example, you could use this property to determine the original source of the data in a query field whose name is unrelated to the name of the field in the underlying table. For details, see the topic "SourceField, SourceTable Properties" in DAO Help. You can set this property for a tabledef with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md).  
  
 `m_strValidationRule`  
 A value that validates the data in a field as it is changed or added to a table. For details, see the topic "ValidationRule Property" in DAO Help. You can set this property for a tabledef with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md).  
  
 For related information about tabledefs, see the **m_strValidationRule** member of the [CDaoTableDefInfo](../vs140/CDaoTableDefInfo-Structure.md) structure.  
  
 `m_strValidationText`  
 A value that specifies the text of the message that your application displays if the value of a DAO field object does not satisfy the validation rule specified by the ValidationRule property setting. For details, see the topic "ValidationText Property" in DAO Help. You can set this property for a tabledef with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md).  
  
 *m_strDefaultValue*  
 The default value of a DAO field object. When a new record is created, the DefaultValue property setting is automatically entered as the value for the field. For details, see the topic "DefaultValue Property" in DAO Help. You can set this property for a tabledef with [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md).  
  
## Remarks  
 The references to Primary, Secondary, and All above indicate how the information is returned by the `GetFieldInfo` member function in classes [CDaoTableDef](../vs140/CDaoTableDef--GetFieldInfo.md), [CDaoQueryDef](../vs140/CDaoQueryDef--GetFieldInfo.md), and [CDaoRecordset](../vs140/CDaoRecordset--GetFieldInfo.md).  
  
 Field objects are not represented by an MFC class. Instead, the DAO objects underlying MFC objects of the following classes contain collections of field objects: [CDaoTableDef](../vs140/CDaoTableDef-Class.md), [CDaoRecordset](../vs140/CDaoRecordset-Class.md), and [CDaoQueryDef](../vs140/CDaoQueryDef-Class.md). These classes supply member functions to access some individual items of field information, or you can access them all at once with a `CDaoFieldInfo` object by calling the `GetFieldInfo` member function of the containing object.  
  
 Besides its use for examining object properties, you can also use `CDaoFieldInfo` to construct an input parameter for creating new fields in a tabledef. Simpler options are available for this task, but if you want finer control, you can use the version of [CDaoTableDef::CreateField](../vs140/CDaoTableDef--CreateField.md) that takes a `CDaoFieldInfo` parameter.  
  
 Information retrieved by the `GetFieldInfo` member function (of the class that contains the field) is stored in a `CDaoFieldInfo` structure. Call the `GetFieldInfo` member function of the containing object in whose Fields collection the field object is stored. `CDaoFieldInfo` also defines a `Dump` member function in debug builds. You can use `Dump` to dump the contents of a `CDaoFieldInfo` object.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CDaoTableDef::GetFieldInfo](../vs140/CDaoTableDef--GetFieldInfo.md)   
 [CDaoRecordset::GetFieldInfo](../vs140/CDaoRecordset--GetFieldInfo.md)   
 [CDaoQueryDef::GetFieldInfo](../vs140/CDaoQueryDef--GetFieldInfo.md)