# DataWS
DataWS is a platform independent library for Data transmission via Web-socket interface. This library provides an easy to use function based interface for creating websocket programs to transmit scientific datasets to browser based visualization and user interfaces. The library is availbe in both C++ and Python versions. The library is header-based. This allows the library to be complied on a large variety of hardware. 


## Example Code



### C++ Code Example:
```CPP
#include "DataWS.h"

using namespace DataWS;

double myDataArray = new double[2048];

int main()
{
DataWS dws;

dws.setupServer("0.0.0.0","1234");  //ip and port to server from 

while(dws.alive())
{
  
dws.sendDoubleArray(myDataArray,sizeof(myDataArray)); //send a double array to a websocket

dws.sendInt(15234);


}
return 0;
}
```

### Python Code Example:
```Python
import DataWS

dws.setupServer("0.0.0.0","1234"); 

```


## Function List


```CPP
alive(); 
```
Returns 1 if no faults in the server. If false returns a negative value.  
