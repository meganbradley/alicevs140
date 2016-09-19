---
title: "CRichEditView::DoPaste"
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
ms.assetid: 39d3df99-f7ec-46ee-bdbd-0eeed48f1811
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRichEditView::DoPaste
Call this function to paste the OLE item in `dataobj` into this rich edit document/view.  
  
## Syntax  
  
```  
  
      void DoPaste(  
   COleDataObject& dataobj,  
   CLIPFORMAT cf,  
   HMETAFILEPICT hMetaPict   
);  
```  
  
#### Parameters  
 `dataobj`  
 The [COleDataObject](../vs140/COleDataObject-Class.md) containing the data to paste.  
  
 `cf`  
 The desired Clipboard format.  
  
 `hMetaPict`  
 The metafile that represents the item to be pasted.  
  
## Remarks  
 The framework calls this function as part of the default implementation of [QueryAcceptData](../vs140/CRichEditView--QueryAcceptData.md).  
  
 This function determines the type of paste based on the results of the handler for Paste Special. If `cf` is 0, the new item uses the current iconic representation. If `cf` is nonzero and `hMetaPict` is not **NULL**, the new item uses `hMetaPict` for its representation.  
  
## Requirements  
 **Header:** afxrich.h  
  
## See Also  
 [CRichEditView Class](../vs140/CRichEditView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRichEditCtrl::Paste](../vs140/CRichEditCtrl--Paste.md)   
 [CRichEditView::IsRichEditFormat](../vs140/CRichEditView--IsRichEditFormat.md)   
 [CRichEditView::InsertItem](../vs140/CRichEditView--InsertItem.md)