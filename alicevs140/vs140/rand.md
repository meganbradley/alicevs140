---
title: "rand"
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
apiname: 
  - rand
apilocation: 
  - msvcr110_clr0400.dll
  - msvcrt.dll
  - msvcr120.dll
  - msvcr80.dll
  - msvcr100.dll
  - msvcr110.dll
  - msvcr90.dll
apitype: DLLExport
ms.assetid: 75d9df25-7aaf-4a88-b940-2775559634e8
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# rand
Generates a pseudorandom number. A more secure version of this function is available, see [rand_s](../vs140/rand_s.md).  
  
## Syntax  
  
```  
int rand( void );  
```  
  
## Return Value  
 `rand` returns a pseudorandom number, as described above. There is no error return.  
  
## Remarks  
 The `rand` function returns a pseudorandom integer in the range 0 to `RAND_MAX` (32767). Use the [srand](../vs140/srand.md) function to seed the pseudorandom-number generator before calling `rand`.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`rand`|<stdlib.h>|  
  
 For additional compatibility information, see [Compatibility](../vs140/Compatibility.md) in the Introduction.  
  
## Example  
  
```  
// crt_rand.c  
// This program seeds the random-number generator  
// with the time, then exercises the rand function.  
//  
  
#include <stdlib.h>  
#include <stdio.h>  
#include <time.h>  
  
void SimpleRandDemo( int n )  
{  
   // Print n random numbers.  
   int i;  
   for( i = 0; i < n; i++ )  
      printf( "  %6d\n", rand() );  
}  
  
void RangedRandDemo( int range_min, int range_max, int n )  
{  
   // Generate random numbers in the half-closed interval  
   // [range_min, range_max). In other words,  
   // range_min <= random number < range_max  
   int i;  
   for ( i = 0; i < n; i++ )  
   {  
      int u = (double)rand() / (RAND_MAX + 1) * (range_max - range_min)  
            + range_min;  
      printf( "  %6d\n", u);  
   }  
}  
  
int main( void )  
{  
   // Seed the random-number generator with the current time so that  
   // the numbers will be different every time we run.  
   srand( (unsigned)time( NULL ) );  
  
   SimpleRandDemo( 10 );  
   printf("\n");  
   RangedRandDemo( -100, 100, 10 );  
}  
```  
  
  **22036**  
 **18330**  
 **11651**  
 **27464**  
 **18093**  
 **3284**  
 **11785**  
 **14686**  
 **11447**  
 **11285**  
 **74**  
 **48**  
 **27**  
 **65**  
 **96**  
 **64**  
 **-5**  
 **-42**  
 **-55**  
 **66**   
## .NET Framework Equivalent  
 [System::Random Class](https://msdn.microsoft.com/en-us/library/system.random.aspx)  
  
## See Also  
 [Floating-Point Support](../vs140/Floating-Point-Support.md)   
 [srand](../vs140/srand.md)   
 [rand_s](../vs140/rand_s.md)