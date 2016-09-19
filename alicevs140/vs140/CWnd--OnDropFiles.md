---
title: "CWnd::OnDropFiles"
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
ms.assetid: e85baebb-c8fa-4020-bc8b-aca481ceb58d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::OnDropFiles
The framework calls this member function when the user releases the left mouse button over a window that has registered itself as the recipient of dropped files.  
  
## Syntax  
  
```  
  
      afx_msg void OnDropFiles(  
   HDROP hDropInfo   
);  
```  
  
#### Parameters  
 *hDropInfo*  
 A pointer to an internal data structure that describes the dropped files. This handle is used by the **DragFinish**, **DragQueryFile**, and **DragQueryPoint** Windows functions to retrieve information about the dropped files.  
  
## Remarks  
 Typically, a derived class will be designed to support dropped files and it will register itself during window construction.  
  
> [!NOTE]
>  This member function is called by the framework to allow your application to handle a Windows message. The parameters passed to your function reflect the parameters received by the framework when the message was received. If you call the base-class implementation of this function, that implementation will use the parameters originally passed with the message and not the parameters you supply to the function.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::DragAcceptFiles](../vs140/CWnd--DragAcceptFiles.md)   
 [WM_DROPFILES](http://msdn.microsoft.com/library/windows/desktop/bb774303)   
 [DragAcceptFiles](http://msdn.microsoft.com/library/windows/desktop/bb776406)   
 [DragFinish](http://msdn.microsoft.com/library/windows/desktop/bb776407)   
 [DragQueryFile](http://msdn.microsoft.com/library/windows/desktop/bb776408)   
 [DragQueryPoint](http://msdn.microsoft.com/library/windows/desktop/bb776409)