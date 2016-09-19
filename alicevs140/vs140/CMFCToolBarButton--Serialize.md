---
title: "CMFCToolBarButton::Serialize"
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
ms.assetid: c1ac1233-85b2-44b3-8230-ca2003467fda
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarButton::Serialize
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
 This method supports data transfer processes such as clipboard or drag-and-drop operations. It reads or writes properties of the button such as the ID, text label, and image ID from or to the provided `CArchive` object.  
  
 For serialization examples, see [Serialization: Serializing an Object](../vs140/Serialization--Serializing-an-Object.md).  
  
## Requirements  
 **Header:** afxtoolbarbutton.h  
  
## See Also  
 [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [CArchive Class](../vs140/CArchive-Class.md)   
 [Serialization: Serializing an Object](../vs140/Serialization--Serializing-an-Object.md)