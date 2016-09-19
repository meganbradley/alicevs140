---
title: "COlePasteSpecialDialog::GetDrawAspect"
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
ms.assetid: 8013427e-2242-4cfb-b66d-ec12567f6fc3
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePasteSpecialDialog::GetDrawAspect
Determines if the user chose to display the selected item as an icon.  
  
## Syntax  
  
```  
  
DVASPECT GetDrawAspect( ) const;  
```  
  
## Return Value  
 The method needed to render the object.  
  
-   `DVASPECT_CONTENT` Returned if the Display As Icon check box was not checked when the dialog box was dismissed.  
  
-   `DVASPECT_ICON` Returned if the Display As Icon check box was checked when the dialog box was dismissed.  
  
## Remarks  
 Only call this function after [DoModal](../vs140/COlePasteSpecialDialog--DoModal.md) returns **IDOK**.  
  
 For more information on drawing aspect, see the [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePasteSpecialDialog Class](../vs140/COlePasteSpecialDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePasteSpecialDialog::DoModal](../vs140/COlePasteSpecialDialog--DoModal.md)