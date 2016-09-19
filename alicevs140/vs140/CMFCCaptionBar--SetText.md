---
title: "CMFCCaptionBar::SetText"
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
ms.assetid: d30224da-af46-41ef-8480-fe446a19490a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCCaptionBar::SetText
Sets the text label for the caption bar.  
  
## Syntax  
  
```  
void SetText(  
   const CString& strText,  
   BarElementAlignment textAlignment=ALIGN_RIGHT   
);  
```  
  
#### Parameters  
 [in] `strText`  
 The text string to set.  
  
 [in] `textAlignment`  
 The text alignment.  
  
## Remarks  
 The text label is aligned as specified by the `textAlignment` parameter. It can be one of the following `BarElementAlignment` values:  
  
-   ALIGN_INVALID  
  
-   ALIGN_LEFT  
  
-   ALIGN_RIGHT  
  
-   ALIGN_CENTER  
  
## Requirements  
 **Header:** afxcaptionbar.h  
  
## See Also  
 [CMFCCaptionBar Class](../vs140/CMFCCaptionBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)