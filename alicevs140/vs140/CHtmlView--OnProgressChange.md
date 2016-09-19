---
title: "CHtmlView::OnProgressChange"
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
ms.assetid: 858d5a0f-8457-448a-bb0d-16fa8e7dcd67
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::OnProgressChange
This member function is called by the framework to notify an application that the progress of a download operation has been updated.  
  
## Syntax  
  
```  
  
      virtual void OnProgressChange(  
   long nProgress,  
   long nProgressMax   
);  
```  
  
#### Parameters  
 *nProgress*  
 Amount of total progress to show, or -1 when progress is complete.  
  
 *nProgressMax*  
 Maximum progress value.  
  
## Remarks  
 The container can use the information provided by this event to display the number of bytes downloaded so far or to update a progress indicator.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::GetBusy](../vs140/CHtmlView--GetBusy.md)   
 [CProgressCtrl Class](../vs140/CProgressCtrl-Class.md)