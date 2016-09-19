---
title: "VsgDbg::~VsgDbg (Destructor)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7a3b97fb-d344-4df7-b195-9347d1edfcf7
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# VsgDbg::~VsgDbg (Destructor)
Destroys an instance of the `VsgDbg` class. If graphics information is actively being recorded, the graphics log file is finalized and closed, and the resources that were used while actively capturing graphics information are released.  
  
## Syntax  
  
```cpp  
~VsgDbg();  
```  
  
## See Also  
 [VsgDbg (Constructor)](../vs140/VsgDbg--VsgDbg--Constructor-.md)