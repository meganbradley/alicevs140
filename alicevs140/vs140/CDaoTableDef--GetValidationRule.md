---
title: "CDaoTableDef::GetValidationRule"
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
ms.assetid: ded6c6cf-8977-46b1-ae99-7b46582fd70c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::GetValidationRule
Call this member function to retrieve the validation rule for a tabledef.  
  
## Syntax  
  
```  
  
CString GetValidationRule( );  
  
```  
  
## Return Value  
 A **CString** object that validates the data in a field as it is changed or added to a table.  
  
## Remarks  
 Validation rules are used in connection with update operations. If a tabledef contains a validation rule, updates to that tabledef must match predetermined criteria before the data is changed. If the change does not match the criteria, an exception containing the value of [GetValidationText](../vs140/CDaoTableDef--GetValidationText.md) is thrown. For a `CDaoTableDef` object, this `CString` is read-only for an attached table and read/write for a base table.  
  
 For related information, see the topic "ValidationRule Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::SetValidationRule](../vs140/CDaoTableDef--SetValidationRule.md)   
 [CDaoTableDef::GetValidationText](../vs140/CDaoTableDef--GetValidationText.md)   
 [CDaoTableDef::SetValidationText](../vs140/CDaoTableDef--SetValidationText.md)