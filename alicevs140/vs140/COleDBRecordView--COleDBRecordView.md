---
title: "COleDBRecordView::COleDBRecordView"
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
ms.assetid: 83f4ae82-dcb1-44aa-865b-3427fb29c34e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDBRecordView::COleDBRecordView
Constructs a `COleDBRecordView` object.  
  
## Syntax  
  
```  
  
      COleDBRecordView(  
   LPCTSTR lpszTemplateName   
);  
COleDBRecordView(  
   UINT nIDTemplate   
);  
```  
  
#### Parameters  
 `lpszTemplateName`  
 Contains a null-terminated string that is the name of a dialog-template resource.  
  
 `nIDTemplate`  
 Contains the ID number of a dialog-template resource.  
  
## Remarks  
 When you create an object of a type derived from `COleDBRecordView`, invoke one of the constructors to create the view object and identify the dialog resource on which the view is based. You can identify the resource either by name (pass a string as the argument to the constructor) or by its ID (pass an unsigned integer as the argument).  
  
> [!NOTE]
>  Your derived class *must* supply its own constructor. In the constructor, invoke the constructor, `COleDBRecordView::COleDBRecordView`, with the resource name or ID as an argument.  
  
## Requirements  
 **Header:** afxoledb.h  
  
## See Also  
 [COleDBRecordView Class](../vs140/COleDBRecordView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)