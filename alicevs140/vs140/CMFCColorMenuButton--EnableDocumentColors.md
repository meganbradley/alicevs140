---
title: "CMFCColorMenuButton::EnableDocumentColors"
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
ms.assetid: f81fec17-6a69-46b4-b3f4-fe5acf24f59a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCColorMenuButton::EnableDocumentColors
Enables the display of document-specific colors instead of system colors.  
  
## Syntax  
  
```  
void EnableDocumentColors(  
   LPCTSTR lpszLabel,  
   BOOL bEnable=TRUE   
);  
```  
  
#### Parameters  
 [in] `lpszLabel`  
 Specifies the button text.  
  
 [in] `bEnable`  
 `TRUE` to display document-specific colors or `FALSE` to display system colors.  
  
## Remarks  
 Use this method to display the current document colors or the system palette colors when the user clicks a color menu button.  
  
## Requirements  
 **Header:** afxcolormenubutton.h  
  
## See Also  
 [CMFCColorMenuButton Class](../vs140/CMFCColorMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)