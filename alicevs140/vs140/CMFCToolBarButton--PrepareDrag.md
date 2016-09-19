---
title: "CMFCToolBarButton::PrepareDrag"
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
ms.assetid: d9638614-fdc1-4119-8bea-bd688d6a4782
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::PrepareDrag
Called by the framework when the button is about to perform a drag-and-drop operation.  
  
## Syntax  
  
```  
virtual BOOL PrepareDrag(  
   COleDataSource& srcItem  
);  
```  
  
#### Parameters  
 [in] `srcItem`  
 A `COleDataSource` object that stores state information about the drag-and-drop operation.  
  
## Return Value  
 `TRUE` if the operation succeeds; otherwise `FALSE`.  
  
## Remarks  
 The framework calls this method to prepare the toolbar button to store its state in the provided `COleDataSource` object. This method stores its state by serializing itself to a shared file and then passing that file to the [COleDataSource::CacheGlobalData](../vs140/COleDataSource--CacheGlobalData.md) method. For more information about toolbar button serialization, see [CMFCToolBarButton::Serialize](../vs140/CMFCToolBarButton--Serialize.md).  
  
 This method does nothing and returns `TRUE` if the button cannot be stored (the [CMFCToolBarButton::CanBeStored](../vs140/CMFCToolBarButton--CanBeStored.md) method returns `FALSE`). It returns `FALSE` if an exception occurs during object serialization.  
  
 For more information about OLE drag-and-drop operations, see [Drag and Drop (OLE)](../vs140/Drag-and-Drop--OLE-.md).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [COleDataSource Class](../Topic/COleDataSource%20Class.md)   
 [CMFCToolBarButton::CanBeStored](../vs140/CMFCToolBarButton--CanBeStored.md)   
 [CMFCToolBarButton::Serialize](../vs140/CMFCToolBarButton--Serialize.md)   
 [Drag and Drop (OLE)](../vs140/Drag-and-Drop--OLE-.md)