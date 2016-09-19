---
title: "Walkthrough: Creating an Image-Processing Network"
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
ms.assetid: 78ccadc9-5ce2-46cc-bd62-ce0f99d356b8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Creating an Image-Processing Network
This document demonstrates how to create a network of asynchronous message blocks that perform image processing.  
  
 The network determines which operations to perform on an image on the basis of its characteristics. This example uses the *dataflow* model to route images through the network. In the dataflow model, independent components of a program communicate with one another by sending messages. When a component receives a message, it can perform some action and then pass the result of that action to another component. Compare this with the *control flow* model, in which an application uses control structures, for example, conditional statements, loops, and so on, to control the order of operations in a program.  
  
 A network that is based on dataflow creates a *pipeline* of tasks. Each stage of the pipeline concurrently performs part of the overall task. An analogy to this is an assembly line for automobile manufacturing. As each vehicle passes through the assembly line, one station assembles the frame, another installs the engine, and so on. By enabling multiple vehicles to be assembled simultaneously, the assembly line provides better throughput than assembling complete vehicles one at a time.  
  
## Prerequisites  
 Read the following documents before you start this walkthrough:  
  
-   [Asynchronous Message Blocks](../vs140/Asynchronous-Message-Blocks.md)  
  
-   [How-to: Use a Message Block Filter to Improve Performance](../vs140/How-to--Use-a-Message-Block-Filter.md)  
  
-   [Walkthrough: Creating a Dataflow Agent](../vs140/Walkthrough--Creating-a-Dataflow-Agent.md)  
  
 We also recommend that you understand the basics of [!INCLUDE[ndptecgdiplus](../vs140/includes/ndptecgdiplus_md.md)] before you start this walkthrough. For more information about [!INCLUDE[ndptecgdiplus](../vs140/includes/ndptecgdiplus_md.md)], see [GDI+](_gdiplus_GDI_start_cpp).  
  
##  <a name="top"></a> Sections  
 This walkthrough contains the following sections:  
  
-   [Defining Image Processing Functionality](#functionality)  
  
-   [Creating the Image Processing Network](#network)  
  
-   [The Complete Example](#complete)  
  
##  <a name="functionality"></a> Defining Image Processing Functionality  
 This section shows the support functions that the image processing network uses to work with images that are read from disk.  
  
 The following functions, `GetRGB` and `MakeColor`, extract and combine the individual components of the given color, respectively.  
  
 [!CODE [concrt-image-processing-filter#2](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#2)]  
  
 The following function, `ProcessImage`, calls the given [std::function](../vs140/function-Class.md) object to transform the color value of each pixel in a [!INCLUDE[ndptecgdiplus](../vs140/includes/ndptecgdiplus_md.md)] [Bitmap](https://msdn.microsoft.com/en-us/library/ms534420.aspx) object. The `ProcessImage` function uses the [concurrency::parallel_for](../vs140/parallel_for-Function.md) algorithm to process each row of the bitmap in parallel.  
  
 [!CODE [concrt-image-processing-filter#3](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#3)]  
  
 The following functions, `Grayscale`, `Sepiatone`, `ColorMask`, and `Darken`, call the `ProcessImage` function to transform the color value of each pixel in a `Bitmap` object. Each of these functions uses a lambda expression to define the color transformation of one pixel.  
  
 [!CODE [concrt-image-processing-filter#4](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#4)]  
  
 The following function, `GetColorDominance`, also calls the `ProcessImage` function. However, instead of changing the value of each color, this function uses [concurrency::combinable](../vs140/combinable-Class.md) objects to compute whether the red, green, or blue color component dominates the image.  
  
 [!CODE [concrt-image-processing-filter#5](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#5)]  
  
 The following function, `GetEncoderClsid`, retrieves the class identifier for the given MIME type of an encoder. The application uses this function to retrieve the encoder for a bitmap.  
  
 [!CODE [concrt-image-processing-filter#6](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#6)]  
  
 [[Top](#top)]  
  
##  <a name="network"></a> Creating the Image Processing Network  
 This section describes how to create a network of asynchronous message blocks that perform image processing on every [!INCLUDE[TLA#tla_jpeg](../vs140/includes/TLA#tla_jpeg_md.md)] (.jpg) image in a given directory. The network performs the following image-processing operations:  
  
1.  For any image that is authored by Tom, convert to grayscale.  
  
2.  For any image that has red as the dominant color, remove the green and blue components and then darken it.  
  
3.  For any other image, apply sepia toning.  
  
 The network applies only the first image-processing operation that matches one of these conditions. For example, if an image is authored by Tom and has red as its dominant color, the image is only converted to grayscale.  
  
 After the network performs each image-processing operation, it saves the image to disk as a bitmap (.bmp) file.  
  
 The following steps show how to create a function that implements this image processing network and applies that network to every [!INCLUDE[TLA#tla_jpeg](../vs140/includes/TLA#tla_jpeg_md.md)] image in a given directory.  
  
#### To create the image processing network  
  
1.  Create a function, `ProcessImages`, that takes the name of a directory on disk.  
  
     [!CODE [concrt-image-processing-filter#7](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#7)]  
  
2.  In the `ProcessImages` function, create a `countdown_event` variable. The `countdown_event` class is shown later in this walkthrough.  
  
     [!CODE [concrt-image-processing-filter#8](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#8)]  
  
3.  Create a [std::map](../vs140/map-Class.md) object that associates a `Bitmap` object with its original file name.  
  
     [!CODE [concrt-image-processing-filter#9](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#9)]  
  
4.  Add the following code to define the members of the image-processing network.  
  
     [!CODE [concrt-image-processing-filter#10](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#10)]  
  
5.  Add the following code to connect the network.  
  
     [!CODE [concrt-image-processing-filter#11](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#11)]  
  
6.  Add the following code to send to the head of the network the full path of each [!INCLUDE[TLA#tla_jpeg](../vs140/includes/TLA#tla_jpeg_md.md)] file in the directory.  
  
     [!CODE [concrt-image-processing-filter#12](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#12)]  
  
7.  Wait for the `countdown_event` variable to reach zero.  
  
     [!CODE [concrt-image-processing-filter#13](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#13)]  
  
 The following table describes the members of the network.  
  
|Member|Description|  
|------------|-----------------|  
|`load_bitmap`|A [concurrency::transformer](../vs140/transformer-Class.md) object that loads a `Bitmap` object from disk and adds an entry to the `map` object to associate the image with its original file name.|  
|`loaded_bitmaps`|A [concurrency::unbounded_buffer](../vs140/unbounded_buffer-Class.md) object that sends the loaded images to the image processing filters.|  
|`grayscale`|A `transformer` object that converts images that are authored by Tom to grayscale. It uses the metadata of the image to determine its author.|  
|`colormask`|A `transformer` object that removes the green and blue color components from images that have red as the dominant color.|  
|`darken`|A `transformer` object that darkens images that have red as the dominant color.|  
|`sepiatone`|A `transformer` object that applies sepia toning to images that are not authored by Tom and are not predominantly red.|  
|`save_bitmap`|A `transformer` object that saves the processed `image` to disk as a bitmap. `save_bitmap` retrieves the original file name from the `map` object and changes its file name extension to .bmp.|  
|`delete_bitmap`|A `transformer` object that frees the memory for the images.|  
|`decrement`|A [concurrency::call](../vs140/call-Class.md) object that acts as the terminal node in the network. It decrements the `countdown_event` object to signal to the main application that an image has been processed.|  
  
 The `loaded_bitmaps` message buffer is important because, as an `unbounded_buffer` object, it offers `Bitmap` objects to multiple receivers. When a target block accepts a `Bitmap` object, the `unbounded_buffer` object does not offer that `Bitmap` object to any other targets. Therefore, the order in which you link objects to an `unbounded_buffer` object is important. The `grayscale`, `colormask`, and `sepiatone` message blocks each use a filter to accept only certain `Bitmap` objects. The `decrement` message buffer is an important target of the `loaded_bitmaps` message buffer because it accepts all `Bitmap` objects that are rejected by the other message buffers. An `unbounded_buffer` object is required to propagate messages in order. Therefore, an `unbounded_buffer` object blocks until a new target block is linked to it and accepts the message if no current target block accepts that message.  
  
 If your application requires that multiple message blocks process the message, instead of just the one message block that first accepts the message, you can use another message block type, such as `overwrite_buffer`. The `overwrite_buffer` class holds one message at a time, but it propagates that message to each of its targets.  
  
 The following illustration shows the image processing network:  
  
 ![Image processing network](../vs140/media/ConcRT_ImageProc.png "ConcRT_ImageProc")  
  
 The `countdown_event` object in this example enables the image processing network to inform the main application when all images have been processed. The `countdown_event` class uses a [concurrency::event](../vs140/event-Class.md) object to signal when a counter value reaches zero. The main application increments the counter every time that it sends a file name to the network. The terminal node of the network decrements the counter after each image has been processed. After the main application traverses the specified directory, it waits for the `countdown_event` object to signal that its counter has reached zero.  
  
 The following example shows the `countdown_event` class:  
  
 [!CODE [concrt-image-processing-filter#14](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#14)]  
  
 [[Top](#top)]  
  
##  <a name="complete"></a> The Complete Example  
 The following code shows the complete example. The `wmain` function manages the [!INCLUDE[ndptecgdiplus](../vs140/includes/ndptecgdiplus_md.md)] library and calls the `ProcessImages` function to process the [!INCLUDE[TLA#tla_jpeg](../vs140/includes/TLA#tla_jpeg_md.md)] files in the `Sample Pictures` directory.  
  
 [!CODE [concrt-image-processing-filter#15](../CodeSnippet/VS_Snippets_ConcRT/concrt-image-processing-filter#15)]  
  
 The following illustration shows sample output. Each source image is above its corresponding modified image.  
  
 ![Sample output for the example](../vs140/media/ConcRT_ImageOut.png "ConcRT_ImageOut")  
  
 `Lighthouse` is authored by Tom Alphin and therefore is converted to grayscale. `Chrysanthemum`, `Desert`, `Koala`, and `Tulips` have red as the dominant color and therefore have the blue and green color components removed and are darkened. `Hydrangeas`, `Jellyfish`, and `Penguins` match the default criteria and therefore are sepia toned.  
  
 [[Top](#top)]  
  
### Compiling the Code  
 Copy the example code and paste it in a Visual Studio project, or paste it in a file that is named `image-processing-network.cpp` and then run the following command in a Visual Studio Command Prompt window.  
  
 **cl.exe /DUNICODE /EHsc image-processing-network.cpp /link gdiplus.lib**  
  
## See Also  
 [Concurrency Runtime Walkthroughs](../vs140/Concurrency-Runtime-Walkthroughs.md)