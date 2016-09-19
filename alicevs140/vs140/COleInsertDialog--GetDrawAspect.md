---
title: "COleInsertDialog::GetDrawAspect"
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
ms.assetid: 780b329f-cd59-4239-a141-431a66d6aabd
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleInsertDialog::GetDrawAspect
Call this function to determine if the user chose to display the selected item as an icon.  
  
## Syntax  
  
```  
  
DVASPECT GetDrawAspect( ) const;  
```  
  
## Return Value  
 The method needed to render the object.  
  
-   `DVASPECT_CONTENT` Returned if the Display As Icon check box was not checked.  
  
-   `DVASPECT_ICON` Returned if the Display As Icon check box was checked.  
  
## Remarks  
 Call this function only if [DoModal](../vs140/COleInsertDialog--DoModal.md) returns **IDOK**.  
  
 For more information on drawing aspect, see [FORMATETC](http://msdn.microsoft.com/library/windows/desktop/ms682177) data structure in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleInsertDialog Class](../vs140/COleInsertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleInsertDialog::DoModal](../vs140/COleInsertDialog--DoModal.md)   
 [COleInsertDialog::COleInsertDialog](../vs140/COleInsertDialog--COleInsertDialog.md)