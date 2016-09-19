---
title: "CDialog::EndDialog"
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
ms.assetid: 49f28795-6181-488a-869c-a44bbd776af2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDialog::EndDialog
Call this member function to terminate a modal dialog box.  
  
## Syntax  
  
```  
  
      void EndDialog(  
   int nResult   
);  
```  
  
#### Parameters  
 `nResult`  
 Contains the value to be returned from the dialog box to the caller of `DoModal`.  
  
## Remarks  
 This member function returns `nResult` as the return value of `DoModal`. You must use the `EndDialog` function to complete processing whenever a modal dialog box is created.  
  
 You can call `EndDialog` at any time, even in [OnInitDialog](../vs140/CDialog--OnInitDialog.md), in which case you should close the dialog box before it is shown or before the input focus is set.  
  
 `EndDialog` does not close the dialog box immediately. Instead, it sets a flag that directs the dialog box to close as soon as the current message handler returns.  
  
## Example  
 [!CODE [NVC_MFCControlLadenDialog#64](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#64)]  
  
 [!CODE [NVC_MFCControlLadenDialog#65](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCControlLadenDialog#65)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDialog Class](../vs140/CDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDialog::DoModal](../vs140/CDialog--DoModal.md)   
 [CDialog::OnOK](../vs140/CDialog--OnOK.md)   
 [CDialog::OnCancel](../vs140/CDialog--OnCancel.md)