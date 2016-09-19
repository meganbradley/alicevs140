---
title: "CEdit::SetHandle"
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
ms.assetid: d77ab538-b233-4386-a07e-2913e5fb0e05
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::SetHandle
Call this function to set the handle to the local memory that will be used by a multiple-line edit control.  
  
## Syntax  
  
```  
  
      void SetHandle(  
   HLOCAL hBuffer   
);  
```  
  
#### Parameters  
 *hBuffer*  
 Contains a handle to the local memory. This handle must have been created by a previous call to the [LocalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366723) Windows function using the **LMEM_MOVEABLE** flag. The memory is assumed to contain a null-terminated string. If this is not the case, the first byte of the allocated memory should be set to 0.  
  
## Remarks  
 The edit control will then use this buffer to store the currently displayed text instead of allocating its own buffer.  
  
 This member function is processed only by multiple-line edit controls.  
  
 Before an application sets a new memory handle, it should use the [GetHandle](../vs140/CEdit--GetHandle.md) member function to get the handle to the current memory buffer and free that memory using the **LocalFree** Windows function.  
  
 `SetHandle` clears the undo buffer (the [CanUndo](../vs140/CEdit--CanUndo.md) member function then returns 0) and the internal modification flag (the [GetModify](../vs140/CEdit--GetModify.md) member function then returns 0). The edit-control window is redrawn.  
  
 You can use this member function in a multiple-line edit control in a dialog box only if you have created the dialog box with the **DS_LOCALEDIT** style flag set.  
  
> [!NOTE]
>  **GetHandle** will not work with Windows 95/98. If you call **GetHandle** in Windows 95/98, it will return **NULL**. **GetHandle** will work as documented under Windows NT, versions 3.51 and later.  
  
 For more information, see [EM_SETHANDLE](http://msdn.microsoft.com/library/windows/desktop/bb761641), [LocalAlloc](http://msdn.microsoft.com/library/windows/desktop/aa366723), and [LocalFree](http://msdn.microsoft.com/library/windows/desktop/aa366730) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 [!CODE [NVC_MFC_CEdit#22](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CEdit#22)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CEdit::CanUndo](../vs140/CEdit--CanUndo.md)   
 [CEdit::GetHandle](../vs140/CEdit--GetHandle.md)   
 [CEdit::GetModify](../vs140/CEdit--GetModify.md)