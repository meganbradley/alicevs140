---
title: "Concurrency::graphics::direct3d Namespace"
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
ms.assetid: be283331-07cf-46e4-91a1-e8aa85d4ec8e
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Concurrency::graphics::direct3d Namespace
Provides the [get_texture](../vs140/Concurrency--graphics--direct3d-namespace-functions.md#get_texture_function) and [make_texture](../vs140/Concurrency--graphics--direct3d-namespace-functions.md#make_texture_function) methods.  
  
## Syntax  
  
```  
namespace direct3d;  
```  
  
## Members  
  
### Functions  
  
|Name<br /><br /> Description|  
|--------------------------|  
|[get_sampler](../vs140/Concurrency--graphics--direct3d-namespace-functions.md#get_sampler_function)<br /><br /> Get the Direct3D sampler state interface on the given accelerator view that represents the specified sampler object.|  
|[get_texture](../vs140/Concurrency--graphics--direct3d-namespace-functions.md#get_texture_function)<br /><br /> Gets the Direct3D texture interface underlying the specified [texture](../vs140/texture-Class.md) object.|  
|[make_sampler](../vs140/Concurrency--graphics--direct3d-namespace-functions.md#make_sampler_function)<br /><br /> Create a sampler from a Direct3D sampler state interface pointer.|  
|[make_texture](../vs140/Concurrency--graphics--direct3d-namespace-functions.md#make_texture_function)<br /><br /> Creates a [texture](../vs140/texture-Class.md) object by using the specified parameters.|  
|[Msad4](../vs140/Concurrency--graphics--direct3d-namespace-functions.md#msad4_function)<br /><br /> Compares a 4-byte reference value and an 8-byte source value and accumulates a vector of 4 sums.|  
  
## Requirements  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency::graphics  
  
## See Also  
 [Concurrency::graphics Namespace](../vs140/Concurrency--graphics-Namespace.md)