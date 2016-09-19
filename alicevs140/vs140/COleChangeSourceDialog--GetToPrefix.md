---
title: "COleChangeSourceDialog::GetToPrefix"
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
ms.assetid: 0568b059-8d79-4137-8b40-a644dbc9eabc
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleChangeSourceDialog::GetToPrefix
Call this function to get the new prefix string for the source.  
  
## Syntax  
  
```  
  
CString GetToPrefix( );  
  
```  
  
## Return Value  
 The new prefix string of the source.  
  
## Remarks  
 Call this function only after [DoModal](../vs140/COleChangeSourceDialog--DoModal.md) returns **IDOK**.  
  
 This value comes directly from the **lpszTo** member of the [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure.  
  
 For more information, see the [OLEUICHANGESOURCE](http://msdn.microsoft.com/library/windows/desktop/ms682160) structure in [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleChangeSourceDialog Class](../vs140/COleChangeSourceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleChangeSourceDialog::GetFromPrefix](../vs140/COleChangeSourceDialog--GetFromPrefix.md)