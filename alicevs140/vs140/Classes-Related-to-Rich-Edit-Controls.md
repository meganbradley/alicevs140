---
title: "Classes Related to Rich Edit Controls"
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
ms.assetid: 4b31c2cc-6ea1-4146-b7c5-b0b5b419f14d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Classes Related to Rich Edit Controls
The [CRichEditView](../vs140/CRichEditView-Class.md), [CRichEditDoc](../vs140/CRichEditDoc-Class.md), and [CRichEditCntrItem](../vs140/CRichEditCntrItem-Class.md) classes provide the functionality of the rich edit control ([CRichEditCtrl](../vs140/CRichEditCtrl-Class.md)) within the context of MFC's document/view architecture. `CRichEditView` maintains the text and formatting characteristic of text. `CRichEditDoc` maintains the list of OLE client items that are in the view. `CRichEditCntrItem` provides container-side access to the OLE client item. To modify the contents of a `CRichEditView`, use [CRichEditView::GetRichEditCtrl](../vs140/CRichEditView--GetRichEditCtrl.md) to access the underlying rich edit control.  
  
## See Also  
 [Using CRichEditCtrl](../vs140/Using-CRichEditCtrl.md)   
 [Controls (MFC)](../vs140/Controls--MFC-.md)