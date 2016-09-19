---
title: "HLSL Property Pages: Output Files"
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
ms.assetid: c5ba1e72-30de-43eb-a15a-5b0ae58e55c2
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HLSL Property Pages: Output Files
To configure the following properties of the HLSL compiler (fxc.exe), use its **Output Files** property. For information about how to access the **Output Files** property page in the HLSL folder, see [How To: Specify Project Properties with Property Pages](../vs140/How-to--Specify-Project-Properties-with-Property-Pages.md).  
  
## UIElement List  
 **Header Variable Name**  
 Specifies the name of an array that is used to encoded HLSL object code. The array is contained in a header file that is output by the HLSL compiler. The name of the header file is specified by the **Header File Name** property.  
  
 This property corresponds to the **/Vn[name]** command-line argument.  
  
 **Header File Name**  
 Specifies the name of the header file that is output by the HLSL compiler. The header contains HLSL object code that is encoded into an array. The name of the array is specified by the **Header Variable Name** property.  
  
 This property corresponds to the **/Fh[name]** command-line argument.  
  
 **Object File Name**  
 Specifies the name of the object file that is output by the HLSL compiler. By default, the value is **$(OutDir)%(Filename).cso**.  
  
 This property corresponds to the **/Fo[name]** command-line argument.  
  
 **Assembler Output**  
 **Assembly-Only Listing (/Fc)** to output just assembly language statements. **Assembly Code and Hex (/Fx)** to output both assembly language statements and the corresponding op-code in hexadecimal. By default, no listing is output.  
  
 **Assembler Output File**  
 Specifies the name of the assembly listing file that is output by the HLSL compiler.  
  
 This property corresponds to the **/Fc[name]** and **/Fx [name]** command-line arguments.  
  
## See Also  
 [HLSL Property Pages](../vs140/HLSL-Property-Pages.md)   
 [HLSL Property Pages: General](../vs140/HLSL-Property-Pages--General.md)   
 [HLSL Property Pages: Advanced](../vs140/HLSL-Property-Pages--Advanced.md)