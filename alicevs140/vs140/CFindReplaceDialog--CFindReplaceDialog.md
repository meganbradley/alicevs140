---
title: "CFindReplaceDialog::CFindReplaceDialog"
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
ms.assetid: b900e5ef-719f-49b0-992e-531d332ca951
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CFindReplaceDialog::CFindReplaceDialog
Constructs a `CFindReplaceDialog` object.  
  
## Syntax  
  
```  
  
CFindReplaceDialog();  
  
```  
  
## Remarks  
 Because the `CFindReplaceDialog` object is a modeless dialog box, you must construct it on the heap by using the `new` operator.  
  
 During destruction, the framework tries to perform a `delete this` on the pointer to the dialog box. If you created the dialog box on the stack, the `this` pointer does not exist and undefined behavior may result.  
  
 For more information on the construction of `CFindReplaceDialog` objects, see the [CFindReplaceDialog](../vs140/CFindReplaceDialog-Class.md) overview. Use the [CFindReplaceDialog::Create](../vs140/CFindReplaceDialog--Create.md) member function to display the dialog box.  
  
## Example  
 [!CODE [NVC_MFCDocView#170](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#170)]  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CFindReplaceDialog Class](../vs140/CFindReplaceDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CFindReplaceDialog::Create](../vs140/CFindReplaceDialog--Create.md)