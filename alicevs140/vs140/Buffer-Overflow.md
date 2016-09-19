---
title: "Buffer Overflow"
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
ms.topic: article
ms.assetid: f2b7e40a-f02b-46d8-a449-51d26fc0c663
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Buffer Overflow
Varying character sizes can cause problems when you put characters into a buffer. Consider the following code, which copies characters from a string, `sz`, into a buffer, `rgch`:  
  
```  
cb = 0;  
while( cb < sizeof( rgch ) )  
    rgch[ cb++ ] = *sz++;  
```  
  
 The question is: Was the last byte copied a lead byte? The following does not solve the problem because it can potentially overflow the buffer:  
  
```  
cb = 0;  
while( cb < sizeof( rgch ) )  
{  
    _mbccpy( rgch + cb, sz );  
    cb += _mbclen( sz );  
    sz = _mbsinc( sz );  
}  
```  
  
 The `_mbccpy` call attempts to do the correct thing — copy the full character, whether it is 1 or 2 bytes. But it does not take into account that the last character copied might not fit the buffer if the character is 2 bytes wide. The correct solution is:  
  
```  
cb = 0;  
while( (cb + _mbclen( sz )) <= sizeof( rgch ) )  
{  
    _mbccpy( rgch + cb, sz );  
    cb += _mbclen( sz );  
    sz = _mbsinc( sz );  
}  
```  
  
 This code tests for possible buffer overflow in the loop test, using `_mbclen` to test the size of the current character pointed to by `sz`. By making a call to the `_mbsnbcpy` function, you can replace the code in the `while` loop with a single line of code. For example:  
  
```  
_mbsnbcpy( rgch, sz, sizeof( rgch ) );  
```  
  
## See Also  
 [MBCS Programming Tips](../vs140/MBCS-Programming-Tips.md)