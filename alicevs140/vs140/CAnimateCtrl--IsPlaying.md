---
title: "CAnimateCtrl::IsPlaying"
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
ms.assetid: 752e7558-26e1-48da-8386-7fdd46511e06
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAnimateCtrl::IsPlaying
Indicates whether an Audio-Video Interleaved (AVI) clip is playing.  
  
## Syntax  
  
```  
BOOL IsPlaying() const;  
```  
  
## Return Value  
 `true` if an AVI clip is playing; otherwise, `false`.  
  
## Remarks  
 This method sends the [ACM_ISPLAYING](http://msdn.microsoft.com/library/windows/desktop/bb761895) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CAnimateCtrl Class](../vs140/CAnimateCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CAnimateCtrl::Play](../vs140/CAnimateCtrl--Play.md)   
 [ACM_ISPLAYING](http://msdn.microsoft.com/library/windows/desktop/bb761895)