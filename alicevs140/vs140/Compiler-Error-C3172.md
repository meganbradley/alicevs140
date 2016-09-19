---
title: "Compiler Error C3172"
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
ms.topic: error-reference
ms.assetid: 1834e2fd-6036-4c33-aff2-b51bc7c99441
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3172
'module_name': cannot specify different idl_module attributes in a project  
  
 [idl_module](../vs140/idl_module.md) attributes with the same name but different `dllname` or `version`parameters were found in two of the files in a compilation. Only one unique `idl_module` attribute can be specified per compilation.  
  
 Identical `idl_module` attributes can be specified in more than one source code file.  
  
 For example, if the following `idl_module` attributes were found:  
  
```  
// C3172.cpp  
[module(name="MyMod")];  
[ idl_module(name="x", dllname="file.dll", version="1.1") ];  
int main() {}  
```  
  
 And then,  
  
```  
// C3172b.cpp  
// compile with: C3172.cpp  
// C3172 expected  
[ idl_module(name="x", dllname="file.dll", version="1.0") ];  
```  
  
 the compiler would generate C3172 (note the different version values).