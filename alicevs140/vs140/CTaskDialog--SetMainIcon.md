---
title: "CTaskDialog::SetMainIcon"
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
ms.assetid: c0250952-640f-4cba-8cec-ee329b3c6b9a
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CTaskDialog::SetMainIcon
Updates the main icon of the `CTaskDialog`.  
  
## Syntax  
  
```  
void SetMainIcon(  
   HICON hMainIcon  
);  
  
void SetMainIcon(  
   LPCWSTR lpszMainIcon  
);  
```  
  
#### Parameters  
 [in] `hMainIcon`  
 The new icon.  
  
 [in] `lpszMainIcon`  
 The new icon.  
  
## Remarks  
 This method throws an exception with the [ENSURE (MFC)](../vs140/ENSURE--MFC-.md) macro if the `CTaskDialog` is displayed or the input parameter is `NULL`.  
  
 A `CTaskDialog` can only accept an `HICON` or `LPCWSTR` as a main icon. You can configure this by setting the `TDF_USE_HICON_MAIN` option in the constructor or in the [CTaskDialog::SetOptions](../vs140/CTaskDialog--SetOptions.md) method. By default, the `CTaskDialog` is configured to use `LPCWSTR` as the input type for the main icon. This method generates an exception if you try to set the icon using the inappropriate type.  
  
## Example  
 [!CODE [NVC_MFC_CTaskDialog#7](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CTaskDialog#7)]  
  
## Requirements  
 **Header:** afxtaskdialog.h  
  
## See Also  
 [CTaskDialog Class](../vs140/CTaskDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CTaskDialog::SetOptions](../vs140/CTaskDialog--SetOptions.md)