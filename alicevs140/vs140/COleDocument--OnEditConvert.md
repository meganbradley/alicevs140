---
title: "COleDocument::OnEditConvert"
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
ms.assetid: 29c8a4d4-72a6-4184-90e7-80f4267bcb09
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDocument::OnEditConvert
Displays the OLE Convert dialog box and converts or activates the currently selected OLE item according to user selections in the dialog box.  
  
## Syntax  
  
```  
  
afx_msg void OnEditConvert( );  
```  
  
## Remarks  
 `OnEditConvert` creates and launches a `COleConvertDialog` Convert dialog box.  
  
 An example of conversion is converting a Microsoft Word document into a WordPad document.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleDocument Class](../vs140/COleDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleDocument::OnUpdateObjectVerbMenu](../vs140/COleDocument--OnUpdateObjectVerbMenu.md)   
 [COleConvertDialog Class](../vs140/COleConvertDialog-Class.md)