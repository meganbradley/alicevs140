---
title: "CMFCDropDownToolbarButton::Serialize"
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
ms.assetid: a9e7d019-d0e8-4260-b38d-189702855a37
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownToolbarButton::Serialize
Reads this object from an archive or writes it to an archive.  
  
## Syntax  
  
```  
virtual void Serialize(  
   CArchive& ar  
);  
```  
  
#### Parameters  
 [in] `ar`  
 The `CArchive` object from which or to which to serialize.  
  
## Remarks  
 This method extends the base class implementation ([CMFCToolBarButton::Serialize](../vs140/CMFCToolBarButton--Serialize.md)) by serializing the resource ID of the parent toolbar. When the archive is loading ([CArchive::IsLoading](../vs140/CArchive--IsLoading.md) returns a nonzero value), this method sets the `m_pToolBar` data member to the toolbar that contains the serialized resource ID.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownToolbarButton Class](../vs140/CMFCDropDownToolbarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CMFCToolBarButton::Serialize](../vs140/CMFCToolBarButton--Serialize.md)   
 [CArchive::IsLoading](../vs140/CArchive--IsLoading.md)