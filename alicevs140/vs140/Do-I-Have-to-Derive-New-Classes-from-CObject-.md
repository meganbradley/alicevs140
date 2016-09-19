---
title: "Do I Have to Derive New Classes from CObject?"
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
ms.assetid: 26021031-feaf-424c-80d1-9547c4409d6a
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Do I Have to Derive New Classes from CObject?
No, you don't.  
  
 Derive a class from [CObject](../vs140/CObject-Class.md) when you need the facilities it provides, such as serialization or dynamic creatability. Many data classes need to be serialized to files, so it's often a good idea to derive them from `CObject`. For an example of a class derived from `CObject`, see the [Scribble sample](../vs140/Visual-C---Samples.md).  
  
## See Also  
 [CObject Class: Frequently Asked Questions](../vs140/CObject-Class--Frequently-Asked-Questions.md)