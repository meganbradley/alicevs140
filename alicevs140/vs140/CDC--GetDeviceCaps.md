---
title: "CDC::GetDeviceCaps"
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
ms.assetid: 9f95b97e-32a3-49aa-8cbd-aa2b598ac7be
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::GetDeviceCaps
Retrieves a wide range of device-specific information about the display device.  
  
## Syntax  
  
```  
  
      int GetDeviceCaps(  
   int nIndex   
) const;  
```  
  
#### Parameters  
 `nIndex`  
 Specifies the type of information to return. See [GetDeviceCaps](http://msdn.microsoft.com/library/windows/desktop/dd144877) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for a list of values.  
  
## Return Value  
 The value of the requested capability if the function is successful.  
  
## Example  
 See the example for [CPrintDialog::GetDefaults](../vs140/CPrintDialog--GetDefaults.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [Escape](http://msdn.microsoft.com/library/windows/desktop/dd162701)