---
title: "CRecordset::SetLockingMode"
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
ms.assetid: 193c5385-7c9a-499e-8b9f-e151eda4aa18
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRecordset::SetLockingMode
Sets the locking mode to "optimistic" locking (the default) or "pessimistic" locking. Determines how records are locked for updates.  
  
## Syntax  
  
```  
  
      void SetLockingMode(  
   UINT nMode   
);  
```  
  
#### Parameters  
 `nMode`  
 Contains one of the following values from the **enum LockMode**:  
  
-   **optimistic** Optimistic locking locks the record being updated only during the call to **Update**.  
  
-   **pessimistic** Pessimistic locking locks the record as soon as **Edit** is called and keeps it locked until the **Update** call completes or you move to a new record.  
  
## Remarks  
 Call this member function if you need to specify which of two record-locking strategies the recordset is using for updates. By default, the locking mode of a recordset is **optimistic**. You can change that to a more cautious **pessimistic** locking strategy. Call `SetLockingMode` after you construct and open the recordset object but before you call **Edit**.  
  
## Requirements  
 **Header:** afxdb.h  
  
## See Also  
 [CRecordset Class](../vs140/CRecordset-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRecordset::Edit](../vs140/CRecordset--Edit.md)   
 [CRecordset::Update](../vs140/CRecordset--Update.md)