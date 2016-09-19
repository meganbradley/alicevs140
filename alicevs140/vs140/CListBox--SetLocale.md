---
title: "CListBox::SetLocale"
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
ms.assetid: d36020fd-64ea-4a31-a20c-c7ba0f3d1d04
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CListBox::SetLocale
Sets the locale identifier for this list box.  
  
## Syntax  
  
```  
  
      LCID SetLocale(  
   LCID nNewLocale   
);  
```  
  
#### Parameters  
 `nNewLocale`  
 The new locale identifier (LCID) value to set for the list box.  
  
## Return Value  
 The previous locale identifier (LCID) value for this list box.  
  
## Remarks  
 If **SetLocale** is not called, the default locale is obtained from the system. This system default locale can be modified by using Control Panel's Regional (or International) application.  
  
## Example  
 [!CODE [NVC_MFC_CListBox#37](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CListBox#37)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CListBox Class](../vs140/CListBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CListBox::GetLocale](../vs140/CListBox--GetLocale.md)