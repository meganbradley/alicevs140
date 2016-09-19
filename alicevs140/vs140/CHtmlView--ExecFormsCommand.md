---
title: "CHtmlView::ExecFormsCommand"
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
ms.assetid: d43222f6-bc31-4dc1-8e89-419a4b8e6ced
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHtmlView::ExecFormsCommand
Executes the specified command using the `IOleCommandTarget::Exec` method.  
  
## Syntax  
  
```  
  
      HRESULT ExecFormsCommand(  
   DWORD dwCommandID,  
   VARIANT* pVarIn,  
   VARIANT* pVarOut  
);  
```  
  
#### Parameters  
 `dwCommandID`  
 The command to be executed. This command must belong to the **CMDSETID3_Forms3** group.  
  
 *pVarIn*  
 Pointer to a **VARIANT** structure containing input arguments. Can be **NULL**.  
  
 *pVarOut*  
 Pointer to a **VARIANT** structure to receive command output. Can be **NULL**.  
  
## Return Value  
 A standard `HRESULT` value. For a complete listing of possible values, see [IOleCommandTarget::Exec](http://msdn.microsoft.com/library/windows/desktop/ms690300) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Remarks  
 **ExecFormsCommand** implements the behavior of the [IOleCommandTarget::Exec](http://msdn.microsoft.com/library/windows/desktop/ms690300) method.  
  
## Requirements  
 **Header:** afxhtml.h  
  
## See Also  
 [CHtmlView Class](../vs140/CHtmlView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CHtmlView::QueryFormsCommand](../vs140/CHtmlView--QueryFormsCommand.md)