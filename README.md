# cfsd-standered-message-senderstamps
This is a repository for organizing the various assignments of sender stamps. 

Version: 0.0

OpenDLV message : opendlv-standard-message-set-v0.9.7.odvd

|            OpenDLV message            | sender stamp |    msg content    | sensor/req/log |      unit       | origin |
| :-----------------------------------: | :----------: | :---------------: | :------------: | :-------------: | ------ |
|     opendlv::proxy::TorqueRequest     |     1501     |    torqueRight    |      req       |    0~2400cNm    |        |
|                                       |     1500     |    torqueLeft     |      req       |    0~2400cNm    |        |
|    opendlv.proxy.WheelSpeedReading    |     1901     |  wheelRareRight   |     sensor     |      Km/h       | CANgw  |
|                                       |     1902     |   wheelRareLeft   |     sensor     |      Km/h       | CANgw  |
|                                       |     1903     |  wheelFrontRight  |     sensor     |      Km/h       | CANgw  |
|                                       |     1904     |  wheelFrontLeft   |     sensor     |      Km/h       | CANgw  |
|  opendlv.proxy.PedalPositionReading   |     1901     |       brake       |     sensor     |        %        | CANgw  |
|                                       |     1902     |     throttle      |     sensor     |        %        | CANgw  |
|                                       |     1922     |    brakeFront     |     sensor     |        %        | CANgw  |
|                                       |     1923     |     brakeRear     |     sensor     |        %        | CANgw  |
|     opendlv.proxy.VoltageReading      |     1921     |      accSoC       |     sensor     | State of Charge | CANgw  |
|  opendlv::proxy::SwitchStateReading   |     1924     |     dlStatus      |     sensor     |       0/1       | CANgw  |
|                                       |     1406     |     asMission     |     sensor     |       0-8       | CANgw  |
|                                       |     1404     |   asRedyToDrive   |      req       |       1/0       |        |
|                                       |     1401     |      asState      |      log       |     states      |        |
|                                       |     1407     |     resStatus     |     sensor     |     0/1*[1]     | CANgw  |
|                                       |     1408     |     resEStop      |     sensor     |    0/128*[1]    | CANgw  |
|                                       |     1409     |    resQuality     |     sensor     |    0-100*[1]    | CANgw  |
|                                       |     1410     |    resButtons     |     sensor     |   1/3/5/7*[1]   | CANgw  |
|                                       |     1499     |   resInitialize   |      req       | Don't Care*[1]  |        |
| opendlv::proxy::GroundSteeringReading |     1200     | steeringPosition  |      log       |       mm        |        |
|                                       |     1206     |   rackPosition    |      log       |       mm        |        |
|    opendlv::proxy::PressureReading    |     1202     |  pressureService  |      log       |       bar       |        |
|                                       |     1205     | pressureRegulator |      log       |       bar       |        |
|                                       |     1201     |  pressureEBSLine  |      log       |       bar       |        |
|                                       |     1203     |  pressureEBSAct   |      log       |       bar       |        |

*[1]: detailed definition see read me at:  https://github.com/chalmersfsd/cfsd-proxy-cangw/tree/cfsd-res