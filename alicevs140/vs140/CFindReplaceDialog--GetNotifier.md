---
title: "CFindReplaceDialog::GetNotifier"
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
ms.assetid: ef19f6ee-b14a-41da-80c8-a01f2b1d3069
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFindReplaceDialog::GetNotifier
Call this function to retrieve a pointer to the current Find Replace dialog box.  
  
## Syntax  
  
```  
  
      static CFindReplaceDialog* PASCAL GetNotifier(  
   LPARAM lParam   
);  
```  
  
#### Parameters  
 `lParam`  
 The **lparam** value passed to the frame window's **OnFindReplace** member function.  
  
## Return Value  
 A pointer to the current dialog box.  
  
## Remarks  
 It should be used within your callback function to access the current dialog box, call its member functions, and access the `m_fr` structure.  
  
## Example  
 See [CFindReplaceDialog::Create](../vs140/CFindReplaceDialog--Create.md) for an example of how to register the OnFindReplace handler to receive notifications from the Find Replace dialog box.  
  
 [!CODE [NVC_MFCDocView#69](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#69)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFindReplaceDialog Class](../vs140/CFindReplaceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)