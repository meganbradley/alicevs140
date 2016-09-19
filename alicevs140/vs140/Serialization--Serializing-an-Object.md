---
title: "Serialization: Serializing an Object"
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
ms.assetid: 1db772b1-ad55-4fcf-b133-126cca082510
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Serialization: Serializing an Object
The article [Serialization: Making a Serializable Class](../vs140/Serialization--Making-a-Serializable-Class.md) shows how to make a class serializable. Once you have a serializable class, you can serialize objects of that class to and from a file via a [CArchive](../vs140/CArchive-Class.md) object. This article explains:  
  
-   [What a CArchive object is](../vs140/What-Is-a-CArchive-Object.md).  
  
-   [Two ways to create a CArchive](../vs140/Two-Ways-to-Create-a-CArchive-Object.md).  
  
-   [How to use the CArchive << and >> operators](../vs140/Using-the-CArchive----and----Operators.md).  
  
-   [Storing and loading CObjects via an archive](../vs140/Storing-and-Loading-CObjects-via-an-Archive.md).  
  
 You can let the framework create the archive for your serializable document or explicitly create the `CArchive` object yourself. You can transfer data between a file and your serializable object by using the << and >> operators for `CArchive` or, in some cases, by calling the `Serialize` function of a `CObject`-derived class.  
  
## See Also  
 [Serialization](../vs140/Serialization-in-MFC.md)