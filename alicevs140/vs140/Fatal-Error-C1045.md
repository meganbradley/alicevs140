---
title: "Fatal Error C1045"
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
ms.assetid: 766c2f89-4ecd-4281-adaa-14b270cc0829
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1045
compiler limit : linkage specifications nested too deeply  
  
 Nested externals exceed the compiler limit. Nested externals are allowed with the external linkage type, such as `extern` "C++". Reduce the number of nested externals to resolve the error.