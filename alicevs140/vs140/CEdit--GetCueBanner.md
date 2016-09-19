---
title: "CEdit::GetCueBanner"
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
ms.assetid: 56984658-049c-4a8f-baa6-e7114d9ce1b9
caps.latest.revision: 19
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::GetCueBanner
Retrieves the text that is displayed as the text cue, or tip, in an edit control when the control is empty.  
  
## Syntax  
  
```  
BOOL GetCueBanner(  
     LPWSTR lpszText,  
     int cchText  
) const;  
  
CString GetCueBanner() const;  
```  
  
#### Parameters  
 [out] `lpszText`  
 A pointer to a string that contains the cue text.  
  
 [in] `cchText`  
 The number of characters that can be received. This number includes the terminating `NULL` character.  
  
## Return Value  
 For the first overload, `true` if the method is successful; otherwise `false`.  
  
 For the second overload, a [CString](../vs140/Using-CString.md) that contains the cue text if the method is successful; otherwise, the empty string ("").  
  
## Remarks  
 This method sends the [EM_GETCUEBANNER](http://msdn.microsoft.com/library/windows/desktop/bb761572) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]. For more information, see the [Edit_GetCueBannerText](http://msdn.microsoft.com/library/windows/desktop/bb761695) macro.  
  
## Requirements  
 **Header:** afxwin.h  
  
 This control is supported in Windows XP and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::SetCueBanner](../vs140/CEdit--SetCueBanner.md)   
 [EM_GETCUEBANNER](http://msdn.microsoft.com/library/windows/desktop/bb761572)   
 [Edit_GetCueBannerText](http://msdn.microsoft.com/library/windows/desktop/bb761695)