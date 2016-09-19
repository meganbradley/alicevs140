---
title: "CMFCOutlookBar::SetMode2003"
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
ms.assetid: 2cb3d634-cb09-4f42-86f5-feda86a59d18
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCOutlookBar::SetMode2003
Specifies whether the behavior of the Outlook bar mimics that of Outlook 2003.  
  
## Syntax  
  
```  
void SetMode2003(  
   BOOL bMode2003=TRUE   
);  
```  
  
#### Parameters  
 [in] `bMode2003`  
 If TRUE, Office 2003 mode is enabled.  
  
## Remarks  
 Use this function to enable or disable Office 2003 mode. In this mode, the Outlook bar has an additional toolbar with a customization button. The behavior of the Outlook bar conforms to the behavior of the Outlook bar in Microsoft Office 2003.  
  
 By default, this mode is disabled.  
  
> [!NOTE]
>  This function must be called before [CMFCOutlookBar::Create](../vs140/CMFCOutlookBar--Create.md).  
  
## Requirements  
 **Header:** afxoutlookbar.h  
  
## See Also  
 [CMFCOutlookBar Class](../vs140/CMFCOutlookBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)