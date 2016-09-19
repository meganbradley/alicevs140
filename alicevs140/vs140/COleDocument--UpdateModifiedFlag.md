---
title: "COleDocument::UpdateModifiedFlag"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 983415e1-8213-4a36-a462-97f7fd9a29d2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::UpdateModifiedFlag
Call this function to mark the document as modified if any of the contained OLE items have been modified.  
  
## Syntax  
  
```  
  
virtual void UpdateModifiedFlag( );  
```  
  
## Remarks  
 This allows the framework to prompt the user to save the document before closing, even if the native data in the document has not been modified.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::SetModifiedFlag](../vs140/CDocument--SetModifiedFlag.md)   
 [COleClientItem::IsModified](../vs140/COleClientItem--IsModified.md)