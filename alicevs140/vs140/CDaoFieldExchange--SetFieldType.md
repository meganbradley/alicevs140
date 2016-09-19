---
title: "CDaoFieldExchange::SetFieldType"
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
ms.assetid: 20454687-582e-4a2c-96dd-6d6444468287
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoFieldExchange::SetFieldType
Call `SetFieldType` in your `CDaoRecordset` class's `DoFieldExchange` override.  
  
## Syntax  
  
```  
  
      void SetFieldType(  
   UINT nFieldType   
);  
```  
  
#### Parameters  
 `nFieldType`  
 A value of the **enum FieldType**, declared in `CDaoFieldExchange`, which can be either of the following:  
  
-   **CDaoFieldExchange::outputColumn**  
  
-   **CDaoFieldExchange::param**  
  
## Remarks  
 Normally, ClassWizard writes this call for you. If you write your own function and are using the wizard to write your `DoFieldExchange` function, add calls to your own function outside the field map. If you do not use the wizard, there will not be a field map. The call precedes calls to DFX functions, one for each field data member of your class, and identifies the field type as **CDaoFieldExchange::outputColumn**.  
  
 If you parameterize your recordset class, you should add DFX calls for all parameter data members (outside the field map) and precede these calls with a call to `SetFieldType`. Pass the value **CDaoFieldExchange::param**. (You can, instead, use a [CDaoQueryDef](../vs140/CDaoQueryDef-Class.md) and set its parameter values.)  
  
 In general, each group of DFX function calls associated with field data members or parameter data members must be preceded by a call to `SetFieldType`. The `nFieldType` parameter of each `SetFieldType` call identifies the type of the data members represented by the DFX function calls that follow the `SetFieldType` call.  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoFieldExchange Class](../vs140/CDaoFieldExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoFieldExchange::IsValidOperation](../vs140/CDaoFieldExchange--IsValidOperation.md)   
 [CDaoRecordset::DoFieldExchange](../vs140/CDaoRecordset--DoFieldExchange.md)