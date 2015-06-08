#  AudioStreamSpeex  
####**Inherits:** [AudioStreamResampled](class_audiostreamresampled)
####**Category:** Core

###  Brief Description  
Speex audio stream driver.

###  Member Functions 
  * void  **[set&#95;file](#set_file)**  **(** [String](class_string) file  **)**
  * [String](class_string)  **[get&#95;file](#get_file)**  **(** **)** const

###  Description  
Speex audio stream driver. Speex is very useful for compressed speech. It allows loading a very large amount of speech in memory at little IO/latency cost.

###  Member Function Description  

#### <a name="set_file">set_file</a>
  * void  **set&#95;file**  **(** [String](class_string) file  **)**

Set the speech file (which is loaded to memory).

#### <a name="get_file">get_file</a>
  * [String](class_string)  **get&#95;file**  **(** **)** const

Return the speech file.


(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
