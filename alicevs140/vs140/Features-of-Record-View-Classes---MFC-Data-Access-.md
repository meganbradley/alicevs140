---
title: "Features of Record View Classes  (MFC Data Access)"
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
ms.assetid: e7b2820f-09c4-483f-83c0-317e8be42bdf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Features of Record View Classes  (MFC Data Access)
You can do form-based data-access programming with class [CFormView](../vs140/CFormView-Class.md), but [CRecordView](../vs140/CRecordView-Class.md) and [CDaoRecordView](../vs140/CDaoRecordView-Class.md) are generally better classes to derive from. In addition to their `CFormView` features, `CRecordView` and `CDaoRecordView`:  
  
-   Provide dialog data exchange (DDX) between the form controls and the associated recordset object.  
  
-   Handle Move First, Move Next, Move Previous, and Move Last commands for navigating through the records in the associated recordset object.  
  
-   Update changes to the current record when the user moves to another record.  
  
 For more information about navigation, see [Record Views: Supporting Navigation in a Record View](../vs140/Supporting-Navigation-in-a-Record-View---MFC-Data-Access-.md).  
  
## See Also  
 [Record Views  (MFC Data Access)](../vs140/Record-Views---MFC-Data-Access-.md)   
 [ODBC Driver List](../vs140/ODBC-Driver-List.md)