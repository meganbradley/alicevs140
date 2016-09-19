---
title: "COleChangeSourceDialog::GetFileName"
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
ms.assetid: 786bc4a3-0dbf-4555-9d0c-bee2870ad265
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleChangeSourceDialog::GetFileName
Call this function to retrieve the file moniker portion of the display name for the linked client item.  
  
## Syntax  
  
```  
  
CString GetFileName( );  
  
```  
  
## Return Value  
 The file moniker portion of the source display name for the [COleClientItem](../vs140/COleClientItem-Class.md) specified in the constructor.  
  
## Remarks  
 The file moniker together with the item moniker gives the complete display name.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleChangeSourceDialog Class](../vs140/COleChangeSourceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleChangeSourceDialog::GetDisplayName](../vs140/COleChangeSourceDialog--GetDisplayName.md)   
 [COleChangeSourceDialog::GetItemName](../vs140/COleChangeSourceDialog--GetItemName.md)