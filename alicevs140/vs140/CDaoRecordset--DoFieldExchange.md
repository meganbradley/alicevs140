---
title: "CDaoRecordset::DoFieldExchange"
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
ms.assetid: fc578a26-82c6-4d07-b331-705d8d716762
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDaoRecordset::DoFieldExchange
The framework calls this member function to automatically exchange data between the field data members of your recordset object and the corresponding columns of the current record on the data source.  
  
## Syntax  
  
```  
  
      virtual void DoFieldExchange(  
   CDaoFieldExchange* pFX   
);  
```  
  
#### Parameters  
 `pFX`  
 Contains a pointer to a `CDaoFieldExchange` object. The framework will already have set up this object to specify a context for the field exchange operation.  
  
## Remarks  
 It also binds your parameter data members, if any, to parameter placeholders in the SQL statement string for the recordset's selection. The exchange of field data, called DAO record field exchange (DFX), works in both directions: from the recordset object's field data members to the fields of the record on the data source, and from the record on the data source to the recordset object. If you are binding columns dynamically, you are not required to implement `DoFieldExchange`.  
  
 The only action you must normally take to implement `DoFieldExchange` for your derived recordset class is to create the class with ClassWizard and specify the names and data types of the field data members. You might also add code to what ClassWizard writes to specify parameter data members. If all fields are to be bound dynamically, this function will be inactive unless you specify parameter data members.  
  
 When you declare your derived recordset class with ClassWizard, the wizard writes an override of `DoFieldExchange` for you, which resembles the following example:  
  
 [!CODE [NVC_MFCDatabase#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDatabase#2)]  
  
## Requirements  
 **Header:** afxdao.h  
  
## See Also  
 [CDaoRecordset Class](../vs140/CDaoRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDaoException Class](../vs140/CDaoException-Class.md)