CANgw - res  cfsd-standered-message-senderstamps

This is a repository for organizing the various assignments of sender stamps. 

Version: 0.2.0

OpenDLV message : opendlv-standard-message-set-v0.9.7.odvd

cfsd extended message: cfsd-extended-message-set-v0.0.1.odvd

|               OpenDLV message               | sender stamp |    msg content    | sensor/req |      unit       | origin      |
| :-----------------------------------------: | :----------: | :---------------: | :--------: | :-------------: | ----------- |
|        opendlv::proxy::TorqueRequest        |     1503     |    torqueRight    |    req     |    0~2400cNm    | StateM      |
|                                             |     1502     |    torqueLeft     |    req     |    0~2400cNm    | StateM      |
|                                             |     1501     |    torqueRight    |    req     |    0~2400cNm    | longCtrl    |
|                                             |     1500     |    torqueLeft     |    req     |    0~2400cNm    | longCtrl    |
|      opendlv::proxy::WheelSpeedReading      |     1901     |  wheelRareRight   |   sensor   |      Km/h       | CANgw-Lynx  |
|                                             |     1902     |   wheelRareLeft   |   sensor   |      Km/h       | CANgw-Lynx  |
|                                             |     1903     |  wheelFrontRight  |   sensor   |      Km/h       | CANgw-Lynx  |
|                                             |     1904     |  wheelFrontLeft   |   sensor   |      Km/h       | CANgw-Lynx  |
|    opendlv::proxy::PedalPositionReading     |     1901     |       brake       |   sensor   |        %        | CANgw-Lynx  |
|                                             |     1902     |     throttle      |   sensor   |        %        | CANgw-Lynx  |
|                                             |     1922     |    brakeFront     |   sensor   |        %        | CANgw-Lynx  |
|                                             |     1923     |     brakeRear     |   sensor   |        %        | CANgw-Lynx  |
|       opendlv::proxy::VoltageReading        |     1921     |      accSoC       |   sensor   | State of Charge | CANgw-Lynx  |
|     opendlv::proxy::SwitchStateReading      |     1924     |     dlStatus      |   sensor   |       0/1       | CANgw-Lynx  |
|                                             |     1906     |     asMission     |   sensor   |       0-8       | CANgw-Lynx  |
|                                             |     1405     |     ebsFault      |   sensor   |      bool       | StateM      |
|                                             |     1401     |      asState      |   sensor   |   states*[2]    | StateM      |
|                                             |     1801     |     resStatus     |   sensor   |     0/1*[1]     | CANgw - res |
|                                             |     1802     |     resEStop      |   sensor   |    0/128*[1]    | CANgw - res |
|                                             |     1803     |    resQuality     |   sensor   |    0-100*[1]    | CANgw - res |
|                                             |     1804     |    resButtons     |   sensor   |   1/3/5/7*[1]   | CANgw - res |
|                                             |     1413     |    steerFault     |   sensor   |      bool       | StateM      |
|                                             |     1414     |     ebsState      |   sensor   |     0-2*[2]     | StateM      |
|                                             |     1415     |   serviceValve    |   sensor   |      bool       | StateM      |
|                                             |     1049     |       ebsOk       |   sensor   |      bool       | ASNode      |
|                                             |     1112     |   clampExtended   |   sensor   |      bool       | ASNode      |
|                                             |     1115     |       asms        |   sensor   |      bool       | ASNode      |
|                                             |   (unset)    |    tsActivated    |   sensor   |      bool       | ASNode      |
|                                             |     1916     |       KnobR       |   sensor   |    1-12 int     | CANgw-Lynx  |
|                                             |     1917     |       NnobL       |   sensor   |    1-12 int     | CANgw-Lynx  |
|     opendlv::proxy::SwitchStateRequest      |     1044     |    ebsSpeaker     |    req     |      bool       | StateM      |
|                                             |     1027     |     heartBeat     |    req     |      bool       | StateM      |
|                                             |     1045     |    compressor     |    req     |      bool       | StateM      |
|                                             |     1066     |  finishedSignal   |    req     |      bool       | StateM      |
|                                             |     1067     |  shutdownSignal   |    req     |      bool       | StateM      |
|                                             |     1099     |   resInitialize   |    req     | Don't Care*[1]  | StateM      |
|                                             |     1404     |  asReadyToDrive   |    req     |       1/0       | StateM      |
|    opendlv::proxy::GroundSteeringReading    |     1200     | steeringPosition  |   sensor   |       mm        | ASNode      |
|                                             |     1206     |   rackPosition    |   sensor   |       mm        | ASNode      |
|       opendlv::proxy::PressureReading       |     1202     |  pressureService  |   sensor   |       bar       | ASNode      |
|                                             |     1205     | pressureRegulator |   sensor   |       bar       | ASNode      |
|                                             |     1201     |  pressureEBSLine  |   sensor   |       bar       | ASNode      |
|                                             |     1203     |  pressureEBSAct   |   sensor   |       bar       | ASNode      |
|                                             |     1509     |    brakeTarget    |   sensor   |                 | StateM      |
|                                             |     1510     |    brakeActual    |   sensor   |                 | StateM      |
| opendlv::proxy::PulseWidthModulationRequest |     1350     |  brakeDutyCycle   |    req     |   dutyCycles    | Brake       |
|                                             |     1341     |  brakeDutyCycle   |    req     |   dutyCycles    | StateM      |
|                                             |     1300     |  blueAssiSignal   |    req     |   dutyCycles    | StateM      |
|                                             |     1320     |   redAssiSignal   |    req     |   dutyCycles    | StateM      |
|                                             |     1321     |  greenAssiSignal  |    req     |   dutyCycles    | StateM      |
|   opendlv::proxy::AngularVelocityReading    |     112      |  angularVelocity  |   sensor   |      rad/s      | imu         |
|     opendlv::proxy::AccelerationReading     |     112      |   acceleration    |   sensor   |      m/s^2      | imu         |
|     opendlv::proxy::GroundSpeedReading      |     112      |    groundSpeed    |   sensor   |       m/s       | imu         |
|    opendlv::proxy::GeodeticWgs84Reading     |     112      |    geolocation    |   sensor   |       deg       | imu         |
|             opendlv::sim::Frame             |     112      |    eulerAngle     |   sensor   |       deg       | imu         |

*[1]: detailed definition see read me at:  https://github.com/chalmersfsd/cfsd-proxy-cangw/tree/cfsd-res  
*[2]: detailed definition see read me at:  https://github.com/chalmersfsd/cfsd-logic-lynx-state-machine/tree/develop

Sender Stamps Mapping:

| Category | Microservice Name - | Offset |
| -------- | ------------------- | ------ |
| Proxy    | IMU                 | 0000   |
|          | ASNode - GPIO       | 1000   |
|          | ASNode - Analog     | 1200   |
|          | ASNode - PWM        | 1300   |
|          | CANgw - Lynx        | 1900   |
|          | CANgw - res         | 1800   |
|          |                     |        |
|          |                     |        |

