# How-to-install-Optical-flow-code-
Hello everyone! I have successfully installed and import caffe having version of 1.0.0. when i download optical flow code from http://www.cs.cmu.edu/~jcwalker/OF/OF.html and try to compile it.It gives me an error. 
Here is the error 
[ 75%] Building CXX object src/caffe/CMakeFiles/caffe.dir/layers/infogain_loss_layer.cpp.o 
[ 75%] Linking CXX static library ../../lib/libcaffe.a 
[ 75%] Built target caffe Scanning dependencies of target upgrade_net_proto_binary.bin 
[ 75%] Building CXX object tools/CMakeFiles/upgrade_net_proto_binary.bin.dir/upgrade_net_proto_binary.cpp.o 
In file included from /home/nonsemantic/softwares/optical_flow_prediction/include/caffe/common_layers.hpp:10:0,                  from /home/nonsemantic/softwares/optical_flow_prediction/include/caffe/vision_layers.hpp:10,                  
from /home/nonsemantic/softwares/optical_flow_prediction/include/caffe/caffe.hpp:16,                  
from /home/nonsemantic/softwares/optical_flow_prediction/tools/upgrade_net_proto_binary.cpp:9: /home/nonsemantic/softwares/optical_flow_prediction/include/caffe/data_layers.hpp:9:18: fatal error: hdf5.h: No such file or directory compilation terminated. tools/CMakeFiles/upgrade_net_proto_binary.bin.dir/build.make:62: recipe for target 'tools/CMakeFiles/upgrade_net_proto_binary.bin.dir/upgrade_net_proto_binary.cpp.o' failed make[2]: *** [tools/CMakeFiles/upgrade_net_proto_binary.bin.dir/upgrade_net_proto_binary.cpp.o] 
Error 1 CMakeFiles/Makefile2:4016: recipe for target 'tools/CMakeFiles/upgrade_net_proto_binary.bin.dir/all' failed make[1]: *** [tools/CMakeFiles/upgrade_net_proto_binary.bin.dir/all] 
Error 2 Makefile:127: recipe for target 'all' failed make: *** [all] Error 2 nonsemantic@nonsemantic-Aspire-E1-571G:~/softwares/optical_flow_prediction/build$  

I have edit Makefile.config 
INCLUDE_DIRS := $(PYTHON_INCLUDE) /usr/local/include /usr/include/hdf5/serial/
LIBRARY_DIRS := $(PYTHON_LIB) /usr/local/lib /usr/lib /usr/lib/x86_64-linux-gnu/hdf5/serial/ 

but it will not help me. 

i have also tried 
$ sudo ln -s /usr/lib/x86_64-linux-gnu/libhdf5_serial.so.10 /usr/lib/x86_64-linux-gnu/libhdf5.so 
$ sudo ln -s /usr/lib/x86_64-linux-gnu/libhdf5_serial_hl.so.10 /usr/lib/x86_64-linux-gnu/libhdf5_hl.so. 
This will not work as well. 
I have ubuntu 16.04 and cuda 8.0 installed, opencv version 2.4. Please suggest me where i am going wrong. Thanks in advance 
