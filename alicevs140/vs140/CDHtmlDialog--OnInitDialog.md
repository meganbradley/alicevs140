---
title: "CDHtmlDialog::OnInitDialog"
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
ms.assetid: 25aa8368-69df-44f1-ae1c-860fa0c6df42
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDHtmlDialog::OnInitDialog
Called in response to the **WM_INITDIALOG** message.  
  
## Syntax  
  
```  
  
virtual BOOL OnInitDialog( );  
  
```  
  
## Return Value  
 The default implementation returns **TRUE**.  
  
## Remarks  
 This message is sent to the dialog box during the **Create**, `CreateIndirect`, or `DoModal` calls, which occur immediately before the dialog box is displayed.  
  
 Override this member function if you need to perform special processing when the dialog box is initialized. In the overridden version, first call the base class `OnInitDialog` but disregard its return value. You will normally return **TRUE** from your overridden member function.  
  
 Windows calls the `OnInitDialog` function through the standard global dialog-box procedure common to all Microsoft Foundation Class Library dialog boxes, rather than through your message map, so you do not need a message-map entry for this member function.  
  
## Requirements  
 **Header:** afxdhtml.h  
  
## See Also  
 [CDHtmlDialog Class](../vs140/CDHtmlDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)