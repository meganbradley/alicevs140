---
title: "CMFCRibbonBaseElement::AddToKeyList"
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
ms.assetid: e96cbf02-9386-4e9a-ac80-3538d56d9465
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCRibbonBaseElement::AddToKeyList
Adds a keytip for the ribbon element to an array of keytips.  
  
## Syntax  
  
```  
virtual void AddToKeyList(  
    CArray<CMFCRibbonKeyTip*, CMFCRibbonKeyTip*>& arElems  
);  
```  
  
#### Parameters  
 [in] `arElems`  
 Reference to a [CArray](../vs140/CArray-Class.md) of keytips.  
  
## Remarks  
 When the ribbon keytips feature is enabled, the framework displays ribbon keytips when the user presses the ALT key or the F10 key.  
  
## Requirements  
 **Header:** afxbaseribbonelement.h  
  
## See Also  
 [CMFCRibbonBaseElement Class](../vs140/CMFCRibbonBaseElement-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)