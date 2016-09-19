---
title: "CDaoTableDef::GetValidationText"
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
ms.assetid: ca4be9a4-101f-4f95-b66f-0f6a6f5235fb
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoTableDef::GetValidationText
Call this function to retrieve the string to display when a user enters data that does not match the validation rule.  
  
## Syntax  
  
```  
  
CString GetValidationText( );  
  
```  
  
## Return Value  
 A `CString` object that specifies the text displayed if the user enters data that does not match the validation rule.  
  
## Remarks  
 For a `CDaoTableDef` object, this `CString` is read-only for an attached table and read/write for a base table.  
  
 For related information, see the topic "ValidationText Property" in DAO Help.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoTableDef Class](../vs140/CDaoTableDef-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoTableDef::SetValidationRule](../vs140/CDaoTableDef--SetValidationRule.md)   
 [CDaoTableDef::SetValidationText](../vs140/CDaoTableDef--SetValidationText.md)   
 [CDaoTableDef::GetValidationRule](../vs140/CDaoTableDef--GetValidationRule.md)