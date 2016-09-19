---
title: "Linker Tools Error LNK1256"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 55b64b2b-a56b-436c-a55e-ec9c6dcb050e
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Linker Tools Error LNK1256
ALINK operation failed : reason  
  
 A common reason for LNK1256 is an incorrect version number for an assembly. The value 65535 is not allowed for any part of the assembly version number. The valid range for assembly versions is 0 – 65534.  
  
 LNK1256 can also be caused if ALINK could not find the named key container. Delete the key container and add it again to the strong name CSP by using [sn.exe](assetId:///c1d2b532-1b8e-4c7a-8ac5-53b801135ec6).  
  
 Another reason for LNK1256 is a version mismatch between the linker and Alink.dll. This can be caused by a corrupted Visual Studio installation. Use **Programs and Features** in the Windows Control Panel to repair or reinstall Visual Studio.  
  
 The following sample generates LNK1256:  
  
```  
// LNK1256.cpp  
// compile with: /clr /LD  
// LNK1256 expected  
[assembly:System::Reflection::AssemblyVersionAttribute("1.0.65535")];  
public class CMyClass {  
public:  
   int value;  
};  
```