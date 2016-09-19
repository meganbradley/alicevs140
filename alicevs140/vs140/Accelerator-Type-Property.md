---
title: "Accelerator Type Property"
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
ms.assetid: 8c349bc4-e6ad-43fa-959e-f29168af35b8
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Accelerator Type Property
The accelerator **Type** property determines whether the shortcut key combination associated with the accelerator ID is a virtual key combination or an ASCII/ANSI key value:  
  
-   If the **Type** property is **ASCII**, the [Modifier](../vs140/Accelerator-Modifier-Property.md) may only be None or Alt, or it can have an accelerator which uses the CTRL key (specified by preceding the key with a ^).  
  
-   If the **Type** property is **VIRTKEY**, any combination of Modifier and Key values is valid.  
  
    > [!NOTE]
    >  If you want to enter a value into the accelerator table and have the value be treated as ASCII/ANSI, simply click the Type for the entry in the table and select ASCII from the drop down list. However, if you use the **Next Key Typed** command (**Edit** menu) to specify the Key, you must change the **Type** property from VIRTKEY to ASCII *before* entering the Key code.  
  
## Requirements  
 Win32  
  
## See Also  
 [Setting Accelerator Properties](../vs140/Setting-Accelerator-Properties.md)   
 [Accelerator Editor](../vs140/Accelerator-Editor.md)