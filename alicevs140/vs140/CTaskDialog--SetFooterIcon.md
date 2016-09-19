---
title: "CTaskDialog::SetFooterIcon"
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
ms.assetid: ace3f2a5-9def-4371-9ef6-a7735193b55b
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetFooterIcon
Updates the footer icon of the `CTaskDialog`.  
  
## Syntax  
  
```  
void SetFooterIcon(  
   HICON hFooterIcon  
);  
  
void SetFooterIcon(  
   LPCWSTR lpszFooterIcon  
);  
```  
  
#### Parameters  
 [in] `hFooterIcon`  
 The new icon for the `CTaskDialog`.  
  
 [in] `lpszFooterIcon`  
 The new icon for the `CTaskDialog`.  
  
## Remarks  
 The footer icon is displayed on the bottom of the [CTaskDialog Class](../vs140/CTaskDialog-Class.md). It can have associated footer text. You can change the footer text with [CTaskDialog::SetFooterText](../vs140/CTaskDialog--SetFooterText.md).  
  
 This method throws an exception with the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro if the `CTaskDialog` is displayed or the input parameter is `NULL`.  
  
 A `CTaskDialog` can only accept an `HICON` or `LPCWSTR` as a footer icon. This is configured by setting the option `TDF_USE_HICON_FOOTER` in the constructor or [CTaskDialog::SetOptions](../vs140/CTaskDialog--SetOptions.md). By default, the `CTaskDialog` is configured to use `LPCWSTR` as the input type for the footer icon. This method generates an exception if you try to set the icon using the inappropriate type.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#7)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::CTaskDialog](../vs140/CTaskDialog--CTaskDialog.md)   
 [CTaskDialog::SetFooterText](../vs140/CTaskDialog--SetFooterText.md)