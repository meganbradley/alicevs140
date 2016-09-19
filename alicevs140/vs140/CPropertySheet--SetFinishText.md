---
title: "CPropertySheet::SetFinishText"
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
ms.assetid: 606e2287-6a71-43de-afd1-63c822264a95
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropertySheet::SetFinishText
Sets the text in the Finish command button.  
  
## Syntax  
  
```  
  
      void SetFinishText(  
   LPCTSTR lpszText   
);  
```  
  
#### Parameters  
 `lpszText`  
 Points to the text to be displayed on the Finish command button.  
  
## Remarks  
 Call `SetFinishText` to display the text on the Finish command button and hide the Next and Back buttons after the user completes action on the last page of the wizard.  
  
## Example  
 [!CODE [NVC_MFCDocView#138](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#138)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPropertySheet Class](../vs140/CPropertySheet-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)