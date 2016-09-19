---
title: "CDaoTableDef::SetValidationText"
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
ms.assetid: fd674476-10b4-453e-9ae6-99ae6a4eccb4
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::SetValidationText
Call this member function to set the exception text of a validation rule for a `CDaoTableDef` object with an underlying base table supported by the Microsoft Jet database engine.  
  
## Syntax  
  
```  
  
      void SetValidationText(   
   LPCTSTR lpszValidationText    
);  
```  
  
#### Parameters  
 *lpszValidationText*  
 A pointer to a string expression that specifies the text displayed if entered data is invalid.  
  
## Remarks  
 You cannot set the validation text of an attached table.  
  
 For related information, see the topic "ValidationText Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::SetValidationRule](../vs140/CDaoTableDef--SetValidationRule.md)   
 [CDaoTableDef::GetValidationText](../vs140/CDaoTableDef--GetValidationText.md)   
 [CDaoTableDef::GetValidationRule](../vs140/CDaoTableDef--GetValidationRule.md)