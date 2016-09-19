---
title: "CDaoTableDef::SetValidationRule"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 08246337-d27b-44ea-93ae-18dc3115df6e
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::SetValidationRule
Call this member function to set a validation rule for a tabledef.  
  
## Syntax  
  
```  
  
      void SetValidationRule(   
   LPCTSTR lpszValidationRule    
);  
```  
  
#### Parameters  
 *lpszValidationRule*  
 A pointer to a string expression that validates an operation.  
  
## Remarks  
 Validation rules are used in connection with update operations. If a tabledef contains a validation rule, updates to that tabledef must match predetermined criteria before the data is changed. If the change does not match the criteria, an exception containing the text of [GetValidationText](../vs140/CDaoTableDef--GetValidationText.md) is displayed.  
  
 Validation is supported only for databases that use the Microsoft Jet database engine. The expression cannot refer to user-defined functions, domain aggregate functions, SQL aggregate functions, or queries. A validation rule for a `CDaoTableDef` object can refer to multiple fields in that object.  
  
 For example, for fields named `hire_date` and `termination_date`, a validation rule might be:  
  
 [!CODE [NVC_MFCDatabase#34](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#34)]  
  
 For related information, see the topic "ValidationRule Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::GetValidationText](../vs140/CDaoTableDef--GetValidationText.md)   
 [CDaoTableDef::SetValidationText](../vs140/CDaoTableDef--SetValidationText.md)   
 [CDaoTableDef::GetValidationRule](../vs140/CDaoTableDef--GetValidationRule.md)