---
title: "Using OLE DB Record Views"
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
ms.assetid: 1cd3e595-ce08-43d8-a0a9-d03b5d3e24ce
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using OLE DB Record Views
If you want to display OLE DB rowset data in an MFC application, you should use the MFC class [COleDBRecordView](../vs140/COleDBRecordView-Class.md). A record view object created from `COleDBRecordView` allows you to display database records in MFC controls. The record view is a dialog form view directly connected to an OLE DB Rowset object created from the `CRowset` template class. Obtaining a handle to the rowset object is simple:  
  
```  
COleDBRecordView myRecordView;  
...  
// CProductAccessor is a user record class  
CRowset<CAccessor<CProductAccessor>> myRowSet = myRecordView.OnGetRowset();  
```  
  
 The view displays the fields of the `CRowset` object in the dialog's controls. The `COleDBRecordView` object uses Dialog Data Exchange (DDX) and the navigational functionality built into `CRowset` (**MoveFirst**, `MoveNext`, `MovePrev`, and `MoveLast`) to automate the movement of data between the controls on the form and the fields of the rowset. `COleDBRecordView` keeps track of the user's position in the rowset so that the record view can update the user interface and supplies an [OnMove](../vs140/COleDBRecordView--OnMove.md) method for updating the current record before moving to another.  
  
 You can use DDX functions with **COleDbRecordView** to get data directly from the database recordset and display it in a dialog control. You should use the **DDX_\*** methods (such as `DDX_Text`), not the **DDX_Field\*** functions (such as `DDX_FieldText`) with **COleDbRecordView**.  
  
## See Also  
 [Using Accessors](../vs140/Using-Accessors.md)   
 [COleDBRecordView Class](../vs140/COleDBRecordView-Class.md)