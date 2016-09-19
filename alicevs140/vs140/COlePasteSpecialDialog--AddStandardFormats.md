---
title: "COlePasteSpecialDialog::AddStandardFormats"
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
ms.assetid: 3c4efa02-d0b2-41e1-b2be-8e20f2034cb2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::AddStandardFormats
Call this function to add the following Clipboard formats to the list of formats your application can support in a Paste Special operation:  
  
## Syntax  
  
```  
  
      void AddStandardFormats(  
   BOOL bEnableLink = TRUE   
);  
```  
  
#### Parameters  
 *bEnableLink*  
 Flag that determines whether to add `CF_LINKSOURCE` to the list of formats your application can paste.  
  
## Remarks  
  
-   **CF_BITMAP**  
  
-   **CF_DIB**  
  
-   `CF_METAFILEPICT`  
  
-   **"Embedded Object"**  
  
-   (optionally) **"Link Source"**  
  
 These formats are used to support embedding and linking.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePasteSpecialDialog::AddFormat](../vs140/COlePasteSpecialDialog--AddFormat.md)