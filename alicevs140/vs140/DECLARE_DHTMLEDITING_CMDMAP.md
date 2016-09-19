---
title: "DECLARE_DHTMLEDITING_CMDMAP"
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
ms.assetid: c66f1d6f-b9e9-449f-81e9-7cd6ab16815c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# DECLARE_DHTMLEDITING_CMDMAP
Declares a DHTML editing command map in a class.  
  
## Syntax  
  
```  
  
DECLARE_DHTMLEDITING_CMDMAP(  
className  
)  
  
```  
  
#### Parameters  
 `className`  
 The name of the class.  
  
## Remarks  
 This macro is to be used in the definition of [CHtmlEditView](../vs140/CHtmlEditView-Class.md)-derived classes.  
  
 Use [BEGIN_DHTMLEDITING_CMDMAP](../vs140/BEGIN_DHTMLEDITING_CMDMAP.md) to implement the map.  
  
## Example  
 See [HTMLEdit Sample](../vs140/Visual-C---Samples.md).  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [DHTML Editing Command Maps](../vs140/DHTML-Editing-Command-Maps.md)