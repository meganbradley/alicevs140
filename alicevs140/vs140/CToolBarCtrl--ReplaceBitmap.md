---
title: "CToolBarCtrl::ReplaceBitmap"
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
ms.assetid: 2ee7fe52-3745-4b00-a618-81aa0d2b6e74
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CToolBarCtrl::ReplaceBitmap
Replaces the existing bitmap in the current toolbar control with a new bitmap.  
  
## Syntax  
  
```  
BOOL ReplaceBitmap(  
     LPTBREPLACEBITMAP pReplaceBitmap  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[in] `pReplaceBitmap`|Pointer to a [TBREPLACEBITMAP](http://msdn.microsoft.com/library/windows/desktop/bb760484) structure that describes the bitmap to be replaced and the new bitmap.|  
  
## Return Value  
 `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 This method sends the [TB_REPLACEBITMAP](http://msdn.microsoft.com/library/windows/desktop/bb787391) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxcmn.h  
  
## Example  
 The following code example replaces the bitmap for the standard toolbar with a different bitmap.  
  
 [!CODE [NVC_MFC_CToolBarCtrl_s1#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CToolbarCtrl_s1#2)]  
  
## See Also  
 [CToolBarCtrl Class](../vs140/CToolBarCtrl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [TB_REPLACEBITMAP](http://msdn.microsoft.com/library/windows/desktop/bb787391)   
 [TBREPLACEBITMAP](http://msdn.microsoft.com/library/windows/desktop/bb760484)   
 [CToolBarCtrl::ChangeBitmap](../vs140/CToolBarCtrl--ChangeBitmap.md)