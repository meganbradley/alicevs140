---
title: "CEditView::SerializeRaw"
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
ms.assetid: d51f6d99-5c0f-4600-9632-946124dcc837
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEditView::SerializeRaw
Call `SerializeRaw` to have a `CArchive` object read or write the text in the `CEditView` object to a text file.  
  
## Syntax  
  
```  
  
      void SerializeRaw(  
   CArchive& ar   
);  
```  
  
#### Parameters  
 `ar`  
 Reference to the `CArchive` object that stores the serialized text.  
  
## Remarks  
 `SerializeRaw` differs from `CEditView`'s internal implementation of `Serialize` in that it reads and writes only the text, without preceding object-description data.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CEditView Class](../vs140/CEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CArchive Class](../vs140/CArchive-Class.md)   
 [CObject::Serialize](../vs140/CObject--Serialize.md)