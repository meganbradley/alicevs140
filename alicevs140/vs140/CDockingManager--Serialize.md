---
title: "CDockingManager::Serialize"
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
ms.assetid: 5bd50e5b-78ad-4835-ad93-5093236a9950
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDockingManager::Serialize
Writes the docking manager to an archive.  
  
## Syntax  
  
```  
void Serialize(  
   CArchive& ar  
);  
```  
  
#### Parameters  
 [in] `ar`  
 A reference to an archive object.  
  
## Remarks  
 Writing the docking manager to an archive involves determining the number of docking control bars and sliders, and writing the control bars, the mini frames, the autohide bars, and the MDI tabbed bars to the archive.  
  
## Requirements  
 **Header:** afxdockingmanager.h  
  
## See Also  
 [CDockingManager Class](../vs140/CDockingManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)