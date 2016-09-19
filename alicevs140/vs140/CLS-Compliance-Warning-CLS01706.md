---
title: "CLS Compliance Warning CLS01706"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b89ccbf1-7256-4842-a0af-44a803f28340
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CLS Compliance Warning CLS01706
Unmanaged pointer types are not CLS-compliant  
  
 A CLS-compliant function signature cannot contain an unmanaged pointer type.  
  
 For more information Common Language Subset (CLS) compliance checking, see [CLS Compliant Assemblies](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 The following sample generates CLS01706:  
  
```  
// CLS01706.cpp  
// compile with: /clr /LD  
// CLS01706 expected  
[assembly:System::CLSCompliant (true)];  
[assembly:System::Reflection::AssemblyKeyFile("clscompliance.snk")];  
  
public ref class One {  
public:  
   void Method1(int* parameter) {}   // CLS01706  
   void Method1(One ^ parameter) {}   // OK  
};  
```