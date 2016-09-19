---
title: "CSimpleStringT::GetBuffer"
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
ms.assetid: 04eadc47-c1a7-420b-81da-35fc90ede986
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::GetBuffer
Returns a pointer to the internal character buffer for the `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
      PXSTR GetBuffer(  
   int nMinBufferLength  
);  
PXSTR GetBuffer();  
```  
  
#### Parameters  
 `nMinBufferLength`  
 The minimum number of characters that the character buffer can hold. This value does not include space for a null terminator.  
  
 If `nMinBufferLength` is larger than the length of the current buffer, `GetBuffer` destroys the current buffer, replaces it with a buffer of the requested size, and resets the object reference count to zero. If you have previously called [LockBuffer](../vs140/CSimpleStringT--LockBuffer.md) on this buffer, you lose the buffer lock.  
  
## Return Value  
 An `PXSTR` pointer to the object's (null-terminated) character buffer.  
  
## Remarks  
 Call this method to return the buffer contents of the `CSimpleStringT` object. The returned `PXSTR` is not a constant and therefore allows direct modification of `CSimpleStringT` contents.  
  
 If you use the pointer returned by `GetBuffer` to change the string contents, you must call [ReleaseBuffer](../vs140/CSimpleStringT--ReleaseBuffer.md) before you use any other `CSimpleStringT` member methods.  
  
 The address returned by `GetBuffer` may not be valid after the call to `ReleaseBuffer` because additional `CSimpleStringT` operations can cause the `CSimpleStringT` buffer to be reallocated. The buffer is not reallocated if you do not change the length of the `CSimpleStringT`.  
  
 The buffer memory is automatically freed when the `CSimpleStringT` object is destroyed.  
  
 If you keep track of the string length yourself, you should not append the terminating null character. However, you must specify the final string length when you release the buffer with `ReleaseBuffer`. If you do append a terminating null character, you should pass –1 (the default) for the length. `ReleaseBuffer` then determines the buffer length.  
  
 If there is insufficient memory to satisfy the `GetBuffer` request, this method throws a CMemoryException*.  
  
## Example  
 [!CODE [NVC_ATLMFC_Utilities#81](../CodeSnippet/VS_Snippets_Cpp/NVC_ATLMFC_Utilities#81)]  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::GetBufferSetLength](../vs140/CSimpleStringT--GetBufferSetLength.md)   
 [CSimpleStringT::ReleaseBuffer](../vs140/CSimpleStringT--ReleaseBuffer.md)