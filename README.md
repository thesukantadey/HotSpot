# HotSpot
HotSpot is an accurate and fast thermal model suitable for use in architectural studies. A simple running instance is shown below.


Get steady-state temperature map:

./hotspot -c hotspot.config -f ev6.flp -p example.ptrace -steady_file example.steady -model_type grid -detailed_3D on -grid_layer_file example.lcf


Transient simulation with steady-state results as initial temperature:

./hotspot -c hotspot.config -init_file example.steady -f ev6.flp -p example.ptrace -o example.ttrace -model_type grid -detailed_3D on -grid_layer_file example.lcf



# For the 3D testcase running instance (following commands are from the inside of 3D_testcase directory)

Get steady-state temperature map:

../hotspot -c ../hotspot.config -f ./ev6_3D_core_layer.flp -p ev6_3D.ptrace -steady_file ev6_3D.steady -model_type grid -detailed_3D on -grid_layer_file ev6_3D.lcf


Transient simulation with steady-state results as initial temperature:

../hotspot -c ../hotspot.config -init_file ev6_3D.steady -f ./ev6_3D_core_layer.flp -p ev6_3D.ptrace -o ev6_3D.ttrace -model_type grid -detailed_3D on -grid_layer_file ev6_3D.lcf

# For plotting using 3Dfig

./3Dfig.pl -a 0.95 -f 10 -s 0 ./example.lcf


