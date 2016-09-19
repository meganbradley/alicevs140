---
title: "CMFCRibbonEdit::CopyFrom"
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
ms.assetid: cfd9bd53-ca6a-4bce-8a87-22f8b8588aae
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonEdit::CopyFrom
Copies the state of the specified [CMFCRibbonEdit](../vs140/CMFCRibbonEdit-Class.md) object to the current [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md) object.  
  
## Syntax  
  
```  
virtual void CopyFrom(  
   const CMFCRibbonBaseElement& src  
);  
```  
  
#### Parameters  
 [in] `src`  
 The source [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md) object.  
  
## Remarks  
 The `src` parameter must be of type [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md).  
  
## Requirements  
 **Header:** afxribbonedit.h  
  
## See Also  
 [CMFCRibbonEdit Class](../vs140/CMFCRibbonEdit-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)