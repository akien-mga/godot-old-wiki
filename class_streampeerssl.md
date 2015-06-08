#  StreamPeerSSL  
####**Inherits:** [StreamPeer](class_streampeer)
####**Category:** Core

###  Brief Description  


###  Member Functions 
  * Error  **[accept](#accept)**  **(** [StreamPeer](class_streampeer) stream  **)**
  * Error  **[connect](#connect)**  **(** [StreamPeer](class_streampeer) stream, [bool](class_bool) validate_certs=false, [String](class_string) for_hostname=""  **)**
  * [int](class_int)  **[get&#95;status](#get_status)**  **(** **)** const
  * void  **[disconnect](#disconnect)**  **(** **)**

###  Numeric Constants  
  * **STATUS_DISCONNECTED** = **0**
  * **STATUS_CONNECTED** = **1**
  * **STATUS_ERROR_NO_CERTIFICATE** = **2**
  * **STATUS_ERROR_HOSTNAME_MISMATCH** = **3**

###  Member Function Description  


(c) Juan Linietsky, Ariel Manzur, Distributed under the terms of the [CC By](https://creativecommons.org/licenses/by/3.0/legalcode) license.
