---
title: "COleChangeIconDialog::GetIconicMetafile"
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
ms.assetid: 93206775-c172-4419-a5b7-b985177575e2
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleChangeIconDialog::GetIconicMetafile
Call this function to get a handle to the metafile that contains the iconic aspect of the selected item.  
  
## Syntax  
  
```  
  
HGLOBAL GetIconicMetafile( ) const;  
```  
  
## Return Value  
 The handle to the metafile containing the iconic aspect of the new icon, if the dialog box was dismissed by choosing **OK**; otherwise, the icon as it was before the dialog was displayed.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleChangeIconDialog Class](../vs140/COleChangeIconDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleChangeIconDialog::DoModal](../vs140/COleChangeIconDialog--DoModal.md)   
 [COleChangeIconDialog::COleChangeIconDialog](../vs140/COleChangeIconDialog--COleChangeIconDialog.md)   
 [COleChangeIconDialog::DoChangeIcon](../vs140/COleChangeIconDialog--DoChangeIcon.md)