---
title: "CDaoRecordset::SetFieldValue"
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
ms.assetid: e34c33a8-5077-4e53-b828-ad1963a98551
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::SetFieldValue
Call this member function to set the value of a field, either by ordinal position or by changing the value of the string.  
  
## Syntax  
  
```  
  
      virtual void SetFieldValue(  
   LPCTSTR lpszName,  
   const COleVariant& varValue   
);  
virtual void SetFieldValue(  
   int nIndex,  
   const COleVariant& varValue   
);  
void SetFieldValue(  
   LPCTSTR lpszName,  
   LPCTSTR lpszValue   
);  
void SetFieldValue(  
   int nIndex,  
   LPCTSTR lpszValue   
);  
```  
  
#### Parameters  
 `lpszName`  
 A pointer to a string containing the name of a field.  
  
 `varValue`  
 A reference to a [COleVariant](../vs140/COleVariant-Class.md) object containing the value of the field's contents.  
  
 `nIndex`  
 An integer that represents the ordinal position of the field in the recordset's Fields collection (zero-based).  
  
 `lpszValue`  
 A pointer to a string containing the value of the field's contents.  
  
## Remarks  
 Use `SetFieldValue` and [GetFieldValue](../vs140/CDaoRecordset--GetFieldValue.md) to dynamically bind fields at run time rather than statically binding columns using the [DoFieldExchange](../vs140/CDaoRecordset--DoFieldExchange.md) mechanism.  
  
 Note that if you are not creating a UNICODE recordset, you must either use a form of `SetFieldValue` that does not contain a `COleVariant` parameter, or the `COleVariant` object must be explicitly declared ANSI. This can be done by using the [COleVariant::COleVariant](../vs140/COleVariant--COleVariant.md)**(** `lpszSrc`**,** `vtSrc` **)** form of constructor with `vtSrc` set to `VT_BSTRT` (ANSI) or by using the **COleVariant** function [SetString](../vs140/COleVariant--SetString.md)**(** `lpszSrc`**,** `vtSrc` **)** with `vtSrc` set to `VT_BSTRT`.  
  
 For related information, see the topics "Field Object" and "Value Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetFieldValue](../vs140/CDaoRecordset--GetFieldValue.md)   
 [CDaoRecordset::m_nParams](../vs140/CDaoRecordset--m_nParams.md)   
 [CDaoRecordset::SetFieldValueNull](../vs140/CDaoRecordset--SetFieldValueNull.md)   
 [COleVariant::COleVariant](../vs140/COleVariant--COleVariant.md)   
 [COleVariant::SetString](../vs140/COleVariant--SetString.md)