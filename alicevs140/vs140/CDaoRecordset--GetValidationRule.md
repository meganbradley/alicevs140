---
title: "CDaoRecordset::GetValidationRule"
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
ms.assetid: 544a1279-020d-4e1d-b5ee-79d0e533ba7d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::GetValidationRule
Call this member function to determine the rule used to validate data.  
  
## Syntax  
  
```  
  
CString GetValidationRule( );  
  
```  
  
## Return Value  
 A `CString` object containing a value that validates the data in a record as it is changed or added to a table.  
  
## Remarks  
 This rule is text-based, and is applied each time the underlying table is changed. If the data is not legal, MFC throws an exception. The returned error message is the text of the ValidationText property of the underlying field object, if specified, or the text of the expression specified by the ValidationRule property of the underlying field object. You can call [GetValidationText](../vs140/CDaoRecordset--GetValidationText.md) to obtain the text of the error message.  
  
 For example, a field in a record that requires the day of the month might have a validation rule such as "DAY BETWEEN 1 AND 31."  
  
 For related information, see the topic "ValidationRule Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoRecordset::GetValidationText](../vs140/CDaoRecordset--GetValidationText.md)