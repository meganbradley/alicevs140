---
title: "COccManager::SetDefaultButton"
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
ms.assetid: 63b26245-a474-4bc2-baec-9a89fe7942aa
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COccManager::SetDefaultButton
Call this function to set the control as the default button.  
  
## Syntax  
  
```  
  
      static void AFX_CDECL SetDefaultButton(  
   CWnd* pWnd,  
   BOOL bDefault   
);  
```  
  
#### Parameters  
 `pWnd`  
 A pointer to the window containing the control.  
  
 `bDefault`  
 Nonzero if the control should become the default button; otherwise zero.  
  
## Return Value  
 Nonzero if successful; otherwise zero.  
  
## Remarks  
  
> [!NOTE]
>  The control must have the **OLEMISC_ACTSLIKEBUTTON** status bit set. For more information on **OLEMISC** flags, see the [OLEMISC](http://msdn.microsoft.com/library/windows/desktop/ms678497) topic in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxocc.h  
  
## See Also  
 [COccManager Class](../vs140/COccManager-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControlSite::SetDefaultButton](../vs140/COleControlSite--SetDefaultButton.md)