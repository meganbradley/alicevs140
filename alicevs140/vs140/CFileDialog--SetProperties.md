---
title: "CFileDialog::SetProperties"
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
ms.assetid: 73a7ae5e-55c6-4f34-9d94-d7bdaae0b735
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFileDialog::SetProperties
Provides a property store that defines the default values to be used for the item being saved.  
  
## Syntax  
  
```  
BOOL SetProperties(  
   LPCWSTR lpszPropList  
);  
```  
  
#### Parameters  
 `lpszPropList`  
 A list of predefined properties separated by ";". For a list of the flags, see the `Flags` section of [OPENFILENAME](assetId:///8cecfd45-f7c1-4f8d-81a0-4e7fecc3b104).  
  
## Remarks  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFileDialog Class](../vs140/CFileDialog-Class.md)