## GATT feature API for bletiny

<br>

GATT(GENERIC ATTRIBUTE PROFILE) describes a service framework using the Attribute Protocol for discovering services, and for reading and writing characteristic values on a peer device. There are 11 features defined in the GATT Profile, and each of the features is mapped to procedures and sub-procedures: 

|   |   | Discover Primary Services By Service UUID | `b disc svc conn=x uuid=x` |
| 3  | Relationship Discovery | Find Included Services | `b find inc_svcs conn=x start=x end=x` |
|   |   | Discover Characteristic by UUID | `b disc chr conn=x start=x end=x uuid=x` |
|   |   | Read Using Characteristic UUID | `b read conn=x start=x end=x uuid=x` |
| 7  | Writing a Characteristic Value  | Write Without Response | `b write conn=x value=0xXX:0xXX no_rsp=1` |
|   |   | Read Long Characteristic Descriptors | `b read conn=x attr=x long=1` |
|   |   | Write Long Characteristic Descriptors | `b write conn=x value=0xXX:0xXX long=1` |



b show conn
```
To show discovered services
```
b show svc
```

To show discovered characteristics
```
b show chr
```

To show connection RSSI
```
b show rssi conn=x
```