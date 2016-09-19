---
title: "Visual Studio Library Overview"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 48910975-7202-462f-a656-de67a4f8b14d
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Visual Studio Library Overview
Visual Studio Library is a set of template-based C++ classes for simplifying the creation of VSPackages in native C++. Visual Studio Library includes complete source code, as a set of C++ header files. The header files are installed in *Visual Studio SDK installation path*\VisualStudioIntegration \Common\Source\CPP\VSL\Include\\.  
  
> [!NOTE]
>  Visual Studio Library relies on the Active Template Library (ATL) for its support of COM objects. For more information, see [Introduction to ATL](../vs140/Introduction-to-ATL.md).  
  
 Visual Studio Library supports unit testing, both for its own code and for your code. Some unit tests are included, as follows:  
  
-   Visual Studio Library unit tests are installed in *Visual Studio SDK installation path*\VisualStudioIntegration\Common\Source\CPP\VSL\UnitTest\\.  
  
-   The base classes for unit tests for your code are in *Visual Studio SDK installation path*\VisualStudioIntegration\Common\Source\CPP\VSL\Include\VSLUnitTest.h.  
  
 Mock implementations of commonly-used COM and Visual Studio interfaces are in the header files, VSLMockSystemInterfaces.h and VSLMockVisualStudioInterfaces.h, which are installed in *Visual Studio SDK installation path*\VisualStudioIntegration\Common\Source\CPP\VSL\Include\\.  
  
## See Also  
 [Using the Visual Studio Library C++ Template Classes](../vs140/Developing-VSPackages-By-Using-the-Visual-Studio-Library.md)