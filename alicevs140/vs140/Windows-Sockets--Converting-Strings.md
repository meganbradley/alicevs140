---
title: "Windows Sockets: Converting Strings"
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
ms.assetid: 9df522b5-6b23-41e0-bb96-e4e623baf141
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Windows Sockets: Converting Strings
This article and two companion articles explain several issues in Windows Sockets programming. This article covers converting strings. The other issues are covered in [Windows Sockets: Blocking](../vs140/Windows-Sockets--Blocking.md) and [Windows Sockets: Byte Ordering](../vs140/Windows-Sockets--Byte-Ordering.md).  
  
 If you use or derive from class [CAsyncSocket](../vs140/CAsyncSocket-Class.md), you will need to manage these issues yourself. If you use or derive from class [CSocket](../vs140/CSocket-Class.md), MFC manages them for you.  
  
## Converting Strings  
 If you communicate between applications that use strings stored in different wide-character formats, such as Unicode or multibyte character sets (MBCS), or between one of these and an application using ANSI character strings, you must manage the conversions yourself under `CAsyncSocket`. The `CArchive` object used with a `CSocket` object manages this conversion for you through the capabilities of class [CString](../vs140/CStringT-Class.md). For more information, see the Windows Sockets specification, located in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
 For more information, see:  
  
-   [Windows Sockets: Using Class CAsyncSocket](../vs140/Windows-Sockets--Using-Class-CAsyncSocket.md)  
  
-   [Windows Sockets: Using Sockets with Archives](../vs140/Windows-Sockets--Using-Sockets-with-Archives.md)  
  
-   [Windows Sockets: Background](../vs140/Windows-Sockets--Background.md)  
  
-   [Windows Sockets: Stream Sockets](../vs140/Windows-Sockets--Stream-Sockets.md)  
  
-   [Windows Sockets: Datagram Sockets](../vs140/Windows-Sockets--Datagram-Sockets.md)  
  
## See Also  
 [Windows Sockets in MFC](../vs140/Windows-Sockets-in-MFC.md)