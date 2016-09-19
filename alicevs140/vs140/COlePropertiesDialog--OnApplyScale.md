---
title: "COlePropertiesDialog::OnApplyScale"
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
ms.assetid: a77791f0-78d3-4ab3-9fa4-26895adb54ed
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COlePropertiesDialog::OnApplyScale
Called by the framework when the scaling value has changed and either OK or Apply was selected.  
  
## Syntax  
  
```  
  
      virtual BOOL OnApplyScale(  
   COleClientItem* pItem,  
   int nCurrentScale,  
   BOOL bRelativeToOrig   
);  
```  
  
#### Parameters  
 `pItem`  
 Pointer to the document item whose properties are being accessed.  
  
 `nCurrentScale`  
 Numerical value of the dialog scale.  
  
 *bRelativeToOrig*  
 Indicates whether scaling applies to the original size of the document item.  
  
## Return Value  
 Nonzero if handled; otherwise 0.  
  
## Remarks  
 The default implementation does nothing. You must override this function to enable the scaling controls.  
  
> [!NOTE]
>  Before the common OLE Object Properties dialog box is displayed, the framework calls this function with a **NULL** for `pItem` and a – 1 for `nCurrentScale`. This is done to determine if the scaling controls should be enabled.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COlePropertiesDialog Class](../vs140/COlePropertiesDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COlePropertiesDialog::DoModal](../vs140/COlePropertiesDialog--DoModal.md)