---
title: "Specifying Levels of Functionality"
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
ms.assetid: 562669ba-c858-4f66-b5f1-b3beeea4f486
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specifying Levels of Functionality
This article describes how to add the following levels of functionality to your [CObject](../vs140/CObject-Class.md)-derived class:  
  
-   [Run-time class information](#_core_to_add_run.2d.time_class_information)  
  
-   [Dynamic creation support](#_core_to_add_dynamic_creation_support)  
  
-   [Serialization support](#_core_to_add_serialization_support)  
  
 For a general description of `CObject` functionality, see the article [Deriving a Class from CObject](../vs140/Deriving-a-Class-from-CObject.md).  
  
#### To add run-time class information  
  
1.  Derive your class from `CObject`, as described in the [Deriving a Class from CObject](../vs140/Deriving-a-Class-from-CObject.md) article.  
  
2.  Use the `DECLARE_DYNAMIC` macro in your class declaration, as shown here:  
  
     [!CODE [NVC_MFCCObjectSample#2](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#2)]  
  
3.  Use the `IMPLEMENT_DYNAMIC` macro in the implementation file (.CPP) of your class. This macro takes as arguments the name of the class and its base class, as follows:  
  
     [!CODE [NVC_MFCCObjectSample#3](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCCObjectSample#3)]  
  
> [!NOTE]
>  Always put `IMPLEMENT_DYNAMIC` in the implementation file (.CPP) for your class. The `IMPLEMENT_DYNAMIC` macro should be evaluated only once during a compilation and therefore should not be used in an interface file (.H) that could potentially be included in more than one file.  
  
#### To add dynamic creation support  
  
1.  Derive your class from `CObject`.  
  
2.  Use the `DECLARE_DYNCREATE` macro in the class declaration.  
  
3.  Define a constructor with no arguments (a default constructor).  
  
4.  Use the `IMPLEMENT_DYNCREATE` macro in the class implementation file.  
  
#### To add serialization support  
  
1.  Derive your class from `CObject`.  
  
2.  Override the `Serialize` member function.  
  
    > [!NOTE]
    >  If you call `Serialize` directly, that is, you do not want to serialize the object through a polymorphic pointer, omit steps 3 through 5.  
  
3.  Use the `DECLARE_SERIAL` macro in the class declaration.  
  
4.  Define a constructor with no arguments (a default constructor).  
  
5.  Use the `IMPLEMENT_SERIAL` macro in the class implementation file.  
  
> [!NOTE]
>  A "polymorphic pointer" points to an object of a class (call it A) or to an object of any class derived from A (say, B). To serialize through a polymorphic pointer, the framework must determine the run-time class of the object it is serializing (B), since it might be an object of any class derived from some base class (A).  
  
 For more details on how to enable serialization when you derive your class from `CObject`, see the articles [Files in MFC](../vs140/Files-in-MFC.md) and [Serialization](../vs140/Serialization-in-MFC.md).  
  
## See Also  
 [Deriving a Class from CObject](../vs140/Deriving-a-Class-from-CObject.md)