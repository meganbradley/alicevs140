---
title: "Serialization (C++-CLI)"
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
ms.topic: article
H1: Serialization (C++/CLI)
ms.assetid: 869010ca-74e1-4989-b409-4643cdb94084
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Serialization (C++-CLI)
Serialization (the process of storing the state of an object or member to a permanent medium) of managed classes (including individual fields or properties) is supported by the <xref:System.SerializableAttribute?qualifyHint=False> and <xref:System.NonSerializedAttribute?qualifyHint=False> classes.  
  
## Remarks  
 Apply the **SerializableAttribute** custom attribute to a managed class to serialize the entire class or apply only to specific fields or properties to serialize parts of the managed class. Use the **NonSerializedAttribute** custom attribute to exempt fields or properties of a managed class from being serialized.  
  
## Example  
  
### Description  
 In the following example, the class `MyClass` (and the property `m_nCount`) is marked as serializable. However, the `m_nData` property is not serialized as indicated by the **NonSerialized** custom attribute:  
  
### Code  
  
```  
// serialization_and_mcpp.cpp  
// compile with: /LD /clr  
using namespace System;  
  
[ Serializable ]  
public ref class MyClass {  
public:  
   int m_nCount;  
private:  
   [ NonSerialized ]  
   int m_nData;  
};  
```  
  
### Comments  
 Note that both attributes can be referenced using their "short name" (**Serializable** and **NonSerialized**). This is further explained in [Applying Attributes](assetId:///dd7604eb-9fa3-4b60-b2dd-b47739fa3148).  
  
## See Also  
 [.NET Programming in C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md)