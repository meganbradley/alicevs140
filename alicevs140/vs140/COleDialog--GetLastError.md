---
title: "COleDialog::GetLastError"
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
ms.assetid: 0319da74-068a-480a-b2e0-1e910c24c245
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleDialog::GetLastError
Call the `GetLastError` member function to get additional error information when `DoModal` returns **IDABORT**.  
  
## Syntax  
  
```  
  
UINT GetLastError( ) const;  
```  
  
## Return Value  
 The error codes returned by `GetLastError` depend on the specific dialog box displayed.  
  
## Remarks  
 See the `DoModal` member function in the derived classes for information about specific error messages.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleDialog Class](../vs140/COleDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleBusyDialog::DoModal](../vs140/COleBusyDialog--DoModal.md)   
 [COleChangeIconDialog::DoModal](../vs140/COleChangeIconDialog--DoModal.md)   
 [COleChangeSourceDialog::DoModal](../vs140/COleChangeSourceDialog--DoModal.md)   
 [COleConvertDialog::DoModal](../vs140/COleConvertDialog--DoModal.md)   
 [COleInsertDialog::DoModal](../vs140/COleInsertDialog--DoModal.md)   
 [COleLinksDialog::DoModal](../vs140/COleLinksDialog--DoModal.md)   
 [COlePasteSpecialDialog::DoModal](../vs140/COlePasteSpecialDialog--DoModal.md)   
 [COlePropertiesDialog::DoModal](../vs140/COlePropertiesDialog--DoModal.md)   
 [COleUpdateDialog::DoModal](../vs140/COleUpdateDialog--DoModal.md)