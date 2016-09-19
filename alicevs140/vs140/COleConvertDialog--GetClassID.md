---
title: "COleConvertDialog::GetClassID"
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
ms.assetid: ec12cd7e-83a9-4599-a35c-8a7434e7e4d7
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleConvertDialog::GetClassID
Call this function to get the **CLSID** associated with the item the user selected in the Convert dialog box.  
  
## Syntax  
  
```  
  
REFCLSID GetClassID( ) const;  
```  
  
## Return Value  
 The **CLSID** associated with the item that was selected in the Convert dialog box.  
  
## Remarks  
 Call this function only after [DoModal](../vs140/COleConvertDialog--DoModal.md) returns **IDOK**.  
  
 For more information, see [CLSID Key](http://msdn.microsoft.com/library/windows/desktop/ms691424) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleConvertDialog Class](../vs140/COleConvertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleConvertDialog::DoModal](../vs140/COleConvertDialog--DoModal.md)