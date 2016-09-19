---
title: "Arguments to main"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 39824fef-05ad-461d-ae82-49447dda8060
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Arguments to main
**ANSI 2.1.2.2.1** The semantics of the arguments to main  
  
 In Microsoft C, the function called at program startup is called **main**. There is no prototype declared for **main**, and it can be defined with zero, two, or three parameters:  
  
```  
int main( void )  
int main( int argc, char *argv[] )  
int main( int argc, char *argv[], char *envp[] )  
```  
  
 The third line above, where **main** accepts three parameters, is a Microsoft extension to the ANSI C standard. The third parameter, **envp**, is an array of pointers to environment variables. The **envp** array is terminated by a null pointer. See [The main Function and Program Execution](../vs140/main-Function-and-Program-Execution.md) for more information about **main** and **envp**.  
  
 The variable **argc** never holds a negative value.  
  
 The array of strings ends with **argv[argc]**, which contains a null pointer.  
  
 All elements of the **argv** array are pointers to strings.  
  
 A program invoked with no command-line arguments will receive a value of one for **argc**, as the name of the executable file is placed in **argv[0]**. (In MS-DOS versions prior to 3.0, the executable-file name is not available. The letter "C" is placed in **argv[0]**.) Strings pointed to by **argv[1]** through **argv[argc – 1]** represent program parameters.  
  
 The parameters **argc** and **argv** are modifiable and retain their last-stored values between program startup and program termination.  
  
## See Also  
 [Environment](../vs140/Environment.md)