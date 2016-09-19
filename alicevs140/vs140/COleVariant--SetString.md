---
title: "COleVariant::SetString"
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
ms.assetid: 1d8c05db-cfe0-4b79-b330-3c5772786430
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleVariant::SetString
Sets the string to a particular type.  
  
## Syntax  
  
```  
  
      void SetString(  
   LPCTSTR lpszSrc,  
   VARTYPE vtSrc   
);  
```  
  
#### Parameters  
 `lpszSrc`  
 A null-terminated string to be copied into the new `COleVariant` object.  
  
 *VtSrc*  
 The **VARTYPE** for the new `COleVariant` object.  
  
## Remarks  
 The parameter `vtSrc` must be `VT_BSTR` (UNICODE) or `VT_BSTRT` (ANSI). `SetString` is typically used to set strings to ANSI, since the default for the [COleVariant::COleVariant](../vs140/COleVariant--COleVariant.md) constructor with a string or string pointer parameter and no **VARTYPE** is UNICODE.  
  
 A DAO recordset in a non-UNICODE build expects strings to be ANSI. Thus, for DAO functions that use `COleVariant` objects, if you are not creating a UNICODE recordset, you must use the **COleVariant::COleVariant(** `lpszSrc`**,** `vtSrc` **)** form of constructor with `vtSrc` set to `VT_BSTRT` (ANSI) or use `SetString` with `vtSrc` set to `VT_BSTRT` to make ANSI strings. For example, the `CDaoRecordset` functions [CDaoRecordset::Seek](../vs140/CDaoRecordset--Seek.md) and [CDaoRecordset::SetFieldValue](../vs140/CDaoRecordset--SetFieldValue.md) use `COleVariant` objects as parameters. These objects must be ANSI if the DAO recordset is not UNICODE.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleVariant Class](../vs140/COleVariant-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleVariant::COleVariant](../vs140/COleVariant--COleVariant.md)   
 [CDaoRecordset::Seek](../vs140/CDaoRecordset--Seek.md)   
 [CDaoRecordset::SetFieldValue](../vs140/CDaoRecordset--SetFieldValue.md)