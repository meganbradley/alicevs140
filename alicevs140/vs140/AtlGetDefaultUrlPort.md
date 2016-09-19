---
title: "AtlGetDefaultUrlPort"
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
ms.topic: reference
ms.assetid: d894e370-0236-4f19-b4a1-eba50c07550b
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# AtlGetDefaultUrlPort
Call this function to get the default port number associated with a particular Internet protocol or scheme.  
  
## Syntax  
  
```  
  
      inline ATL_URL_PORT AtlGetDefaultUrlPort(  
   ATL_URL_SCHEME m_nScheme   
) throw( );  
```  
  
#### Parameters  
 *m_nScheme*  
 The [ATL_URL_SCHEME](../vs140/ATL_URL_SCHEME.md) value identifying the scheme for which you want to obtain the port number.  
  
## Return Value  
 The [ATL_URL_PORT](../vs140/ATL_URL_PORT.md) associated with the specified scheme or ATL_URL_INVALID_PORT_NUMBER if the scheme is not recognized.  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Functions Alphabetical Reference](../vs140/ATL-Functions-Alphabetical-Reference.md)