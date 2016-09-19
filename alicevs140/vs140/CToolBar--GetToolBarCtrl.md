---
title: "CToolBar::GetToolBarCtrl"
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
ms.assetid: 34cea1c6-ffcd-4dbc-b072-a3faaf0beeaa
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBar::GetToolBarCtrl
This member function allows direct access to the underlying common control.  
  
## Syntax  
  
```  
  
CToolBarCtrl& GetToolBarCtrl( ) const;  
  
```  
  
## Return Value  
 A reference to a `CToolBarCtrl` object.  
  
## Remarks  
 Use `GetToolBarCtrl` to take advantage of the functionality of the Windows toolbar common control, and to take advantage of the support [CToolBarCtrl](../vs140/CToolBarCtrl-Class.md) provides for toolbar customization.  
  
 For more information about using common controls, see the article [Controls](../vs140/Controls--MFC-.md) and [Common Controls](http://msdn.microsoft.com/library/windows/desktop/bb775493) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFCDocViewSDI#15](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocViewSDI#15)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CToolBar Class](../vs140/CToolBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)