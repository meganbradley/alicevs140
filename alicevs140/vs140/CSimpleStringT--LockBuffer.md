---
title: "CSimpleStringT::LockBuffer"
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
ms.assetid: 33066295-9634-432e-bd72-56a6bd2ade36
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::LockBuffer
Disables reference counting and protects the string in the buffer.  
  
## Syntax  
  
```  
PXSTR LockBuffer( );  
```  
  
## Return Value  
 A pointer to a `CSimpleStringT` object or a null-terminated string.  
  
## Remarks  
 Call this method to lock the buffer of the `CSimpleStringT` object. By calling `LockBuffer`, you create a copy of the string, with a –1 for the reference count. When the reference count value is -1, the string in the buffer is considered to be in a "locked" state. While in a locked state, the string is protected in two ways:  
  
-   No other string can get a reference to the data in the locked string, even if that string is assigned to the locked string.  
  
-   The locked string will never reference another string, even if that other string is copied to the locked string.  
  
 By locking the string in the buffer, you ensure that the string's exclusive hold on the buffer will remain intact.  
  
 After you have finished with `LockBuffer`, call [UnlockBuffer](../vs140/CSimpleStringT--UnlockBuffer.md) to reset the reference count to 1.  
  
> [!NOTE]
>  If you call [GetBuffer](../vs140/CSimpleStringT--GetBuffer.md) on a locked buffer and you set the `GetBuffer` parameter `nMinBufferLength` to greater than the length of the current buffer, you will lose the buffer lock. Such a call to `GetBuffer` destroys the current buffer, replaces it with a buffer of the requested size, and resets the reference count to zero.  
  
 For more information about reference counting, see the following articles:  
  
-   [Managing Object Lifetimes through Reference Counting](http://msdn.microsoft.com/library/windows/desktop/ms687260) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]  
  
-   [Implementing Reference Counting](http://msdn.microsoft.com/library/windows/desktop/ms693431) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]  
  
-   [Rules for Managing Reference Counts](http://msdn.microsoft.com/library/windows/desktop/ms692481) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)]  
  
## Example  
 The following example demonstrates the use of `CSimpleStringT::LockBuffer`.  
  
 [!CODE [NVC_ATLMFC_Utilities#85](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#85)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::ReleaseBuffer](../vs140/CSimpleStringT--ReleaseBuffer.md)