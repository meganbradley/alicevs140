---
title: "COleConvertDialog::GetIconicMetafile"
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
ms.assetid: e214714a-4fa6-449f-9e5b-98bab7d1236f
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleConvertDialog::GetIconicMetafile
Call this function to get a handle to the metafile that contains the iconic aspect of the selected item.  
  
## Syntax  
  
```  
  
HGLOBAL GetIconicMetafile( ) const;  
```  
  
## Return Value  
 The handle to the metafile containing the iconic aspect of the selected item, if the Display As Icon check box was checked when the dialog was dismissed by choosing **OK**; otherwise **NULL**.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleConvertDialog Class](../vs140/COleConvertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleConvertDialog::DoModal](../vs140/COleConvertDialog--DoModal.md)   
 [COleConvertDialog::COleConvertDialog](../vs140/COleConvertDialog--COleConvertDialog.md)   
 [COleConvertDialog::GetDrawAspect](../vs140/COleConvertDialog--GetDrawAspect.md)