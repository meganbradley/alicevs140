---
title: "CDaoRecordset::SetParamValue"
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
ms.assetid: 2b3f233e-98b8-4a44-b61c-05f1c49cad71
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::SetParamValue
Call this member function to set the value of a parameter in the recordset at run time.  
  
## Syntax  
  
```  
  
      virtual void SetParamValue(  
   int nIndex,  
   const COleVariant& varValue   
);  
virtual void SetParamValue(  
   LPCTSTR lpszName,  
   const COleVariant& varValue   
);  
```  
  
#### Parameters  
 `nIndex`  
 The numerical position of the parameter in the querydef's Parameters collection.  
  
 `var`  
 The value to set; see Remarks.  
  
 `lpszName`  
 The name of the parameter whose value you want to set.  
  
## Remarks  
 The parameter must already have been established as part of the recordset's SQL string. You can access the parameter either by name or by its index position in the collection.  
  
 Specify the value to set as a `COleVariant` object. For information about setting the desired value and type in your `COleVariant` object, see class [COleVariant](../vs140/COleVariant-Class.md). Note that if you are not creating a UNICODE recordset, the `COleVariant` object must be explicitly declared ANSI. This can be done by using the [COleVariant::COleVariant](../vs140/COleVariant--COleVariant.md)**(** `lpszSrc`**,** `vtSrc` **)** form of constructor with `vtSrc` set to `VT_BSTRT` (ANSI) or by using the **COleVariant** function [SetString](../vs140/COleVariant--SetString.md)**(** `lpszSrc`**,** `vtSrc` **)** with `vtSrc` set to `VT_BSTRT`.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetParamValue](../vs140/CDaoRecordset--GetParamValue.md)   
 [CDaoRecordset::m_nParams](../vs140/CDaoRecordset--m_nParams.md)   
 [CDaoRecordset::SetParamValueNull](../vs140/CDaoRecordset--SetParamValueNull.md)