---
title: "CComboBox::GetCueBanner"
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
ms.assetid: 308b9c92-8e70-43cc-ae14-b1904362d270
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComboBox::GetCueBanner
Gets the cue text that is displayed for a combo box control.  
  
## Syntax  
  
```  
CString GetCueBanner() const;  
BOOL GetCueBanner(  
     LPTSTR lpszText,   
     int cchText  
) const;  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|[out] `lpszText`|Pointer to a buffer that receives the cue banner text.|  
|[in] `cchText`|Size of the buffer that the `lpszText` parameter points to.|  
  
## Return Value  
 In the first overload, a [CString](../vs140/Using-CString.md) object that contains the cue banner text if it exists; otherwise, a `CString` object that has zero length.  
  
 -or-  
  
 In the second overload, `true` if this method is successful; otherwise, `false`.  
  
## Remarks  
 Cue text is a prompt that is displayed in the input area of the combo box control. The cue text is displayed until the user provides input.  
  
 This method sends the [CB_GETCUEBANNER](http://msdn.microsoft.com/library/windows/desktop/bb775843) message, which is described in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxwin.h  
  
 This method is supported in [!INCLUDE[windowsver](../vs140/includes/windowsver_md.md)] and later.  
  
 Additional requirements for this method are described in [Build Requirements for Vista Common Controls](../vs140/Build-Requirements-for-Windows-Vista-Common-Controls.md).  
  
## See Also  
 [CComboBox Class](../vs140/CComboBox-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CComboBox::SetCueBanner](../vs140/CComboBox--SetCueBanner.md)   
 [CB_GETCUEBANNER](http://msdn.microsoft.com/library/windows/desktop/bb775843)