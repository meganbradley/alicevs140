---
title: "PROPPAGEID"
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
ms.topic: article
ms.assetid: ecffa330-cc16-4473-abab-2d0b7f86edd3
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# PROPPAGEID
Adds a property page for use by your OLE control.  
  
## Syntax  
  
```  
  
PROPPAGEID(  
clsid )  
```  
  
#### Parameters  
 `clsid`  
 The unique class ID of a property page.  
  
## Remarks  
 All `PROPPAGEID` macros must be placed between the `BEGIN_PROPPAGEIDS` and `END_PROPPAGEIDS` macros in your control's implementation file.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_PROPPAGEIDS](../vs140/BEGIN_PROPPAGEIDS.md)   
 [END_PROPPAGEIDS](../vs140/END_PROPPAGEIDS.md)