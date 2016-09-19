---
title: "COleChangeSourceDialog::GetFromPrefix"
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
ms.assetid: 87ab7ded-0e32-45d5-86d4-9d86d3e52346
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleChangeSourceDialog::GetFromPrefix
Call this function to get the previous prefix string for the source.  
  
## Syntax  
  
```  
  
CString GetFromPrefix( );  
  
```  
  
## Return Value  
 The previous prefix string of the source.  
  
## Remarks  
 Call this function only after [DoModal](../vs140/COleChangeSourceDialog--DoModal.md) returns **IDOK**.  
  
 This value comes directly from the **lpszFrom** member of the [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure.  
  
 For more information, see the [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleChangeSourceDialog Class](../vs140/COleChangeSourceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleChangeSourceDialog::GetToPrefix](../vs140/COleChangeSourceDialog--GetToPrefix.md)