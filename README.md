# DataWS
DataWS is a platform independent library for Data transmission via Web-socket interface. This library provides an easy to use function based interface for creating websocket programs to transmit scientific datasets to browser based visualization and user interfaces. The library is availbe in both C++ and Python versions. The library is header-based. This allows the library to be complied on a large variety of hardware. 



## Example Code

```CPP
#include "DataWS.h"

using namespace DataWS;

double myDataArray = new double[2048];

int main()
{
DataWS dws;

while(dws.alive())
{
  
dws.sendDoubleArray(myDataArray,sizeof(myDataArray));


}
return 0;
}
```

## Function List


