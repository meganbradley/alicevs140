---
title: "Effects of Buffering"
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
ms.assetid: 5d544812-e95e-4f28-b15a-edef3f3414fd
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Effects of Buffering
The following example shows the effects of buffering. You might expect the program to print `please wait`, wait 5 seconds, and then proceed. It will not necessarily work this way, however, because the output is buffered.  
  
```  
// effects_buffering.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <time.h>  
using namespace std;  
  
int main( )  
{  
   time_t tm = time( NULL ) + 5;  
   cout << "Please wait...";  
   while ( time( NULL ) < tm )  
      ;  
   cout << "\nAll done" << endl;  
}  
```  
  
 To make the program work logically, the `cout` object must empty itself when the message is to appear. To flush an `ostream` object, send it the `flush` manipulator:  
  
```  
cout << "Please wait..." << flush;  
```  
  
 This step flushes the buffer, ensuring the message prints before the wait. You can also use the `endl` manipulator, which flushes the buffer and outputs a carriage return–linefeed, or you can use the `cin` object. This object (with the `cerr` or `clog` objects) is usually tied to the `cout` object. Thus, any use of `cin` (or of the `cerr` or `clog` objects) flushes the `cout` object.  
  
## See Also  
 [Output Streams](../vs140/Output-Streams.md)