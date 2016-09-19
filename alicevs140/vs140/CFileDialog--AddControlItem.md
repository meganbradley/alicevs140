---
title: "CFileDialog::AddControlItem"
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
ms.assetid: 9c82e025-ac28-4f54-8ab4-ca2e65bf2804
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::AddControlItem
Adds an item to a container control in the dialog.  
  
## Syntax  
  
```  
HRESULT AddControlItem(  
   DWORD dwIDCtl,  
   DWORD dwIDItem,  
   const CString& strLabel  
);  
```  
  
#### Parameters  
 `dwIDCtl`  
 The ID of the container control to add the item to.  
  
 `dwIDItem`  
 The ID of the item.  
  
 `strLabel`  
 Item's text.  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)