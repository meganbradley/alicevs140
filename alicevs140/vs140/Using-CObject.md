---
title: "Using CObject"
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
ms.assetid: d0cd19bb-2856-4b41-abbc-620fd64cb223
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using CObject
[CObject](../vs140/CObject-Class.md) is the root base class for most of the Microsoft Foundation Class Library (MFC). The `CObject` class contains many useful features that you may want to incorporate into your own program objects, including serialization support, run-time class information, and object diagnostic output. If you derive your class from `CObject`, your class can exploit these `CObject` features.  
  
## What do you want to do?  
  
-   [Derive a class from CObject](../vs140/Deriving-a-Class-from-CObject.md)  
  
-   [Add support for run-time class information, dynamic creation, and serialization to my derived class](../vs140/Specifying-Levels-of-Functionality.md)  
  
-   [Access run-time class information](../vs140/Accessing-Run-Time-Class-Information.md)  
  
-   [Create objects dynamically](../vs140/Dynamic-Object-Creation.md)  
  
-   [Dump the object's data for diagnostic purposes](assetId:///727855b1-5a83-44bd-9fe3-f1d535584b59)  
  
-   Validate the object's internal state (see [MFC ASSERT_VALID and CObject::AssertValid](assetId:///7654fb75-9e9a-499a-8165-0a96faf2d5e6))  
  
-   [Have the class serialize itself to persistent storage](../vs140/Serialization-in-MFC.md)  
  
-   See a list of [CObject Frequently Asked Questions](../vs140/CObject-Class--Frequently-Asked-Questions.md)  
  
## See Also  
 [Concepts](../vs140/MFC-Concepts.md)   
 [General MFC Topics](../vs140/General-MFC-Topics.md)   
 [CRuntimeClass Structure](../vs140/CRuntimeClass-Structure.md)   
 [Files](../vs140/Files-in-MFC.md)   
 [Serialization](../vs140/Serialization-in-MFC.md)