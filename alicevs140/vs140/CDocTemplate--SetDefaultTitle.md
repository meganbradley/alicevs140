---
title: "CDocTemplate::SetDefaultTitle"
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
ms.assetid: f122f478-a0b0-4854-932e-9fa179528e95
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocTemplate::SetDefaultTitle
Call this function to load the document's default title and display it in the document's title bar.  
  
## Syntax  
  
```  
  
      virtual void SetDefaultTitle(  
   CDocument* pDocument   
) = 0;  
```  
  
#### Parameters  
 *pDocument*  
 Pointer to the document whose title is to be set.  
  
## Remarks  
 For information on the default title, see the description of **CDocTemplate::docName** in [CDocTemplate::GetDocString](../vs140/CDocTemplate--GetDocString.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocTemplate Class](../vs140/CDocTemplate-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocTemplate::GetDocString](../vs140/CDocTemplate--GetDocString.md)