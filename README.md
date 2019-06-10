During testing your code you are are often confronted with the need to examine  
the actual content of an object. Either using ZWRITE or $system.OBJ.Dump()  
you get a picture of simple properties as "--- attribute values ---"  
while "--- swizzled references ---" ar more confusing than informative  
and with "--- calculated references ---" you are just left in the lurch.  
  
This small helper class allows you to dump an object to terminal or  
e.g in background to some stream for later review.  
By default you see just properties with content,  
.   DO ##class(%Z.obj).dumpToDevice(obj)  
or if explicitly requested all properties.  
.    DO ##class(%Z.obj).dumpToDevice(obj,1)  
