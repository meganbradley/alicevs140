---
title: "CReBar::GetReBarCtrl"
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
ms.assetid: 14524576-bb2f-4742-ae53-e449dd7fd5d0
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CReBar::GetReBarCtrl
This member function allows direct access to the underlying common control.  
  
## Syntax  
  
```  
  
CReBarCtrl& GetReBarCtrl( ) const;  
  
```  
  
## Return Value  
 A reference to a [CReBarCtrl](../vs140/CReBarCtrl-Class.md) object.  
  
## Remarks  
 Call this member function to take advantage of the functionality of the Windows rebar common control in customizing your rebar. When you call `GetReBarCtrl`, it returns a reference object to the `CReBarCtrl` object so you can use either set of member functions.  
  
 For more information about using `CReBarCtrl` to customize your rebar, see [Using CReBarCtrl](../vs140/Using-CReBarCtrl.md).  
  
## Example  
 [!CODE [NVC_MFC_CReBarCtrl#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CReBarCtrl#2)]  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CReBar Class](../vs140/CReBar-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)