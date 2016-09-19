---
title: "CDaoParameterInfo Structure"
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
ms.assetid: 45fd53cd-cb84-4e12-b48d-7f2979f898ad
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoParameterInfo Structure
The `CDaoParameterInfo` structure contains information about a parameter object defined for data access objects (DAO).  
  
## Syntax  
  
```  
  
      struct CDaoParameterInfo  
{  
   CString m_strName;       // Primary  
   short m_nType;           // Primary  
   ColeVariant m_varValue;  // Secondary  
};  
```  
  
#### Parameters  
 `m_strName`  
 Uniquely names the parameter object. For more information, see the topic "Name Property" in DAO Help.  
  
 `m_nType`  
 A value that indicates the data type of a parameter object. For a list of the possible values, see the `m_nType` member of the [CDaoFieldInfo](../vs140/CDaoFieldInfo-Structure.md) structure. For more information, see the topic "Type Property" in DAO Help.  
  
 *m_varValue*  
 The value of the parameter, stored in a [COleVariant](../vs140/COleVariant-Class.md) object.  
  
## Remarks  
 The references to Primary and Secondary above indicate how the information is returned by the [GetParameterInfo](../vs140/CDaoQueryDef--GetParameterInfo.md) member function in class `CDaoQueryDef`.  
  
 MFC does not encapsulate DAO parameter objects in a class. DAO querydef objects underlying MFC `CDaoQueryDef` objects store parameters in their Parameters collections. To access the parameter objects in a [CDaoQueryDef](../vs140/CDaoQueryDef-Class.md) object, call the querydef object's `GetParameterInfo` member function for a particular parameter name or an index into the Parameters collection. You can use the [CDaoQueryDef::GetParameterCount](../vs140/CDaoQueryDef--GetParameterCount.md) member function in conjunction with `GetParameterInfo` to loop through the Parameters collection.  
  
 Information retrieved by the [CDaoQueryDef::GetParameterInfo](../vs140/CDaoQueryDef--GetParameterInfo.md) member function is stored in a `CDaoParameterInfo` structure. Call `GetParameterInfo` for the querydef object in whose Parameters collection the parameter object is stored.  
  
> [!NOTE]
>  If you want to get or set only the value of a parameter, use the [GetParamValue](../vs140/CDaoRecordset--GetParamValue.md) and [SetParamValue](../vs140/CDaoRecordset--SetParamValue.md) member functions of class `CDaoRecordset`.  
  
 `CDaoParameterInfo` also defines a `Dump` member function in debug builds. You can use `Dump` to dump the contents of a `CDaoParameterInfo` object.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [Structures, Styles, Callbacks, and Message Maps](../vs140/Structures--Styles--Callbacks--and-Message-Maps.md)   
 [CDaoQueryDef Class](../vs140/CDaoQueryDef-Class.md)