---
title: "Command Handlers for Record Scrolling  (MFC Data Access)"
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
ms.topic: article
ms.assetid: f8b13477-2a37-459e-a30c-806fb78165ac
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command Handlers for Record Scrolling  (MFC Data Access)
Classes [CRecordView](../vs140/CRecordView-Class.md) and [CDaoRecordView](../vs140/CDaoRecordView-Class.md) provide default command handling for the following standard commands:  
  
-   **ID_RECORD_MOVE_FIRST**  
  
-   **ID_RECORD_MOVE_LAST**  
  
-   **ID_RECORD_MOVE_NEXT**  
  
-   **ID_RECORD_MOVE_PREV**  
  
 The `OnMove` member function of classes `CRecordView` and `CDaoRecordView` provides default command handling for all four commands, which move from record to record. As these commands are issued, RFX (or DFX) loads the new record into the recordset's fields and DDX moves the values into the record form's controls. For information about RFX, see [Record Field Exchange (RFX)](../vs140/Record-Field-Exchange--RFX-.md).  
  
> [!NOTE]
>  Be sure to use these standard command IDs for any user-interface objects associated with the standard record navigation commands.  
  
## See Also  
 [Supporting Navigation in a Record View](../vs140/Supporting-Navigation-in-a-Record-View---MFC-Data-Access-.md)