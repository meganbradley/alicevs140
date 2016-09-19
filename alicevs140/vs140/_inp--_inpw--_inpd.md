---
title: "_inp, _inpw, _inpd"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
apiname: 
  - _inp
  - _inpw
  - _inpd
apilocation: 
  - msvcrt.dll
  - msvcr120.dll
  - msvcr110_clr0400.dll
  - msvcr110.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 5d9c2e38-fc85-4294-86d5-7282cc02d1b3
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# _inp, _inpw, _inpd
Inputs, from a port, a byte (`_inp`), a word (`_inpw`), or a double word (`_inpd`).  
  
> [!IMPORTANT]
>  These functions are obsolete. Beginning in Visual Studio 2015, they are not available in the CRT.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the Windows Runtime. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
int _inp(   
   unsigned short port   
);  
unsigned short _inpw(   
   unsigned short port   
);  
unsigned long _inpd(   
   unsigned short port   
);  
```  
  
#### Parameters  
 `port`  
 I/O port number.  
  
## Return Value  
 The functions return the byte, word, or double word read from `port`. There is no error return.  
  
## Remarks  
 The `_inp`, `_inpw`, and `_inpd` functions read a byte, a word, and a double word, respectively, from the specified input port. The input value can be any unsigned short integer in the range 0 – 65,535.  
  
 Because these functions read directly from an I/O port, they might not be used in user code in Windows NT, Windows 2000, Windows XP, and Windows Server 2003.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_inp`|<conio.h>|  
|`_inpw`|<conio.h>|  
|`_inpd`|<conio.h>|  
  
 For more compatibility information, see [Compatibility](../vs140/Compatibility.md).  
  
## Libraries  
 All versions of the [C run-time libraries](../vs140/CRT-Library-Features.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](assetId:///15926806-f0b7-487e-93a6-4e9367ec689f).  
  
## See Also  
 [Console and Port I/O](../vs140/Console-and-Port-I-O.md)   
 [_outp, _outpw, _outpd](../vs140/_outp--_outpw--_outpd.md)