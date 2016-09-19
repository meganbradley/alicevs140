---
title: "COleConvertDialog::GetSelectionType"
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
ms.assetid: ba39c5e5-9102-4f6a-bd6c-f76fa0b18c70
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleConvertDialog::GetSelectionType
Call this function to determine the type of conversion selected in the Convert dialog box.  
  
## Syntax  
  
```  
  
UINT GetSelectionType( ) const;  
```  
  
## Return Value  
 Type of selection made.  
  
## Remarks  
 The return type values are specified by the **Selection** enumeration type declared in the `COleConvertDialog` class.  
  
 `enum Selection`  
  
 `{`  
  
 `noConversion,`  
  
 `convertItem,`  
  
 `activateAs`  
  
 `};`  
  
 Brief descriptions of these values follow:  
  
-   **COleConvertDialog::noConversion** Returned if either the dialog box was canceled or the user selected no conversion. If `COleConvertDialog::DoModal` returned **IDOK**, it is possible that the user selected a different icon than the one previously selected.  
  
-   **COleConvertDialog::convertItem** Returned if the Convert To radio button was checked, the user selected a different item to convert to, and `DoModal` returned **IDOK**.  
  
-   **COleConvertDialog::activateAs** Returned if the Activate As radio button was checked, the user selected a different item to activate, and `DoModal` returned **IDOK**.  
  
## Requirements  
 **Header:** afxodlgs.h  
  
## See Also  
 [COleConvertDialog Class](../vs140/COleConvertDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleConvertDialog::DoModal](../vs140/COleConvertDialog--DoModal.md)   
 [COleConvertDialog::COleConvertDialog](../vs140/COleConvertDialog--COleConvertDialog.md)