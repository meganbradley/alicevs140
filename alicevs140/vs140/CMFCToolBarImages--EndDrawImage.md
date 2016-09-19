---
title: "CMFCToolBarImages::EndDrawImage"
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
ms.assetid: 5a4c77b2-fe12-4f47-9cde-bcab400c7720
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarImages::EndDrawImage
Frees system resources that [CMFCToolBarImages::PrepareDrawImage](../vs140/CMFCToolBarImages--PrepareDrawImage.md) allocated after you draw a toolbar image by calling [CMFCToolBarImages::Draw](../vs140/CMFCToolBarImages--Draw.md).  
  
## Syntax  
  
```  
void EndDrawImage(  
   CAfxDrawState& ds   
);  
```  
  
#### Parameters  
 [in] `ds`  
 A reference to the `CAfxDrawState` object that was passed to the `PrepareDrawImage` method.  
  
## Requirements  
 **Header:** afxtoolbarimages.h  
  
## See Also  
 [CMFCToolBarImages Class](../vs140/CMFCToolBarImages-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)