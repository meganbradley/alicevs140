---
title: "Predefined Rules"
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
ms.assetid: 638cdc3f-4aba-4b4f-96e3-ad65b0364f12
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Predefined Rules
Predefined inference rules use NMAKE-supplied command and options macros.  
  
|Rule|Command|Default<br /><br /> action|Batch<br /><br /> Rule|Platform nmake runs on|  
|----------|-------------|------------------------|--------------------|----------------------------|  
|.asm.exe|$(AS) $(AFLAGS) $<|ml $<|no|x86|  
|.asm.obj|$(AS) $(AFLAGS) /c $<|ml /c $<|yes|x86|  
|.asm.exe|$(AS) $(AFLAGS) $<|ml64 $<|no|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
|.asm.obj|$(AS) $(AFLAGS) /c $<|ml64 /c $<|yes|[!INCLUDE[vcprx64](../vs140/includes/vcprx64_md.md)]|  
|.c.exe|$(CC) $(CFLAGS) $<|cl $<|no|all|  
|.c.obj|$(CC) $(CFLAGS) /c $<|cl /c $<|yes|all|  
|.cc.exe|$(CC) $(CFLAGS) $<|cl $<|no|all|  
|.cc.obj|$(CC) $(CFLAGS) /c $<|cl /c $<|yes|all|  
|.cpp.exe|$(CPP) $(CPPFLAGS) $<|cl $<|no|all|  
|.cpp.obj|$(CPP) $(CPPFLAGS) /c $<|cl /c $<|yes|all|  
|.cxx.exe|$(CXX) $(CXXFLAGS) $<|cl $<|no|all|  
|.cxx.obj|$(CXX) $(CXXFLAGS) /c $<|cl /c $<|yes|all|  
|.rc.res|$(RC) $(RFLAGS) /r $<|rc /r $<|no|all|  
  
## See Also  
 [Inference Rules](../vs140/Inference-Rules.md)