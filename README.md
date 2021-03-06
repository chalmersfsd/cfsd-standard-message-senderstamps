CANgw - res  cfsd-standered-message-senderstamps

This is a repository for organizing the various assignments of sender stamps. 


Rules of the Sender Stamp:

​	If it is a **sensor** data, The sender stamp offset is set by mapping from **origin** microservices

​	else if it is a **request**, the sender stamp offset is set by mapping from **destination** microservices

Version: 0.2.0

OpenDLV message : opendlv-standard-message-set-v0.9.7.odvd

cfsd extended message: cfsd-extended-message-set-v0.0.1.odvd

|               OpenDLV message               | sender stamp |       msg content       | sensor/req |      unit       | origin      | Desitnation |
| :-----------------------------------------: | :----------: | :---------------------: | :--------: | :-------------: | ----------- | ----------- |
|    opendlv::cfsdProxy::TorqueRequestDual    |     1910     | torqueLeft&torqueRight  |    req     |    0~2400cNm    | StateM      | CANgw-Lynx  |
|                                             |     2101     | torqueLeft&torqueRight  |    req     |    0~2400cNm    | longCtrl    | StateM      |
| opendlv::proxy::AxleAngularVelocityReading  |     1901     |     wheelRareRight      |   sensor   |      Km/h       | CANgw-Lynx  |             |
|                                             |     1902     |      wheelRareLeft      |   sensor   |      Km/h       | CANgw-Lynx  |             |
|                                             |     1903     |     wheelFrontRight     |   sensor   |      Km/h       | CANgw-Lynx  |             |
|                                             |     1904     |     wheelFrontLeft      |   sensor   |      Km/h       | CANgw-Lynx  |             |
|                                             |     1933     | motorSpeedEstimateRight |   sensor   |       RPM       | CANgw-Lynx  |             |
|                                             |     1935     | motorSpeedEstimateLeft  |   sensor   |       RPM       | CANgw-Lynx  |             |
|    opendlv::proxy::PedalPositionReading     |     1901     |          brake          |   sensor   |        %        | CANgw-Lynx  |             |
|                                             |     1902     |        throttle         |   sensor   |        %        | CANgw-Lynx  |             |
|                                             |     1922     |       brakeFront        |   sensor   |        %        | CANgw-Lynx  |             |
|                                             |     1923     |        brakeRear        |   sensor   |        %        | CANgw-Lynx  |             |
|       opendlv::proxy::VoltageReading        |     1921     |         accSoC          |   sensor   | State of Charge | CANgw-Lynx  |             |
|     opendlv::proxy::SwitchStateReading      |     1924     |        dlStatus         |   sensor   |       0/1       | CANgw-Lynx  |             |
|                                             |     1906     |        asMission        |   sensor   |     0-8*[2]     | CANgw-Lynx  |             |
|                                             |     2105     |        ebsFault         |   sensor   |      bool       | StateM      |             |
|                                             |     2101     |         asState         |   sensor   |     0-5*[2]     | StateM      |             |
|                                             |     1801     |        resStatus        |   sensor   |     0/1*[1]     | CANgw - res |             |
|                                             |     1802     |        resEStop         |   sensor   |    0/128*[1]    | CANgw - res |             |
|                                             |     1803     |       resQuality        |   sensor   |    0-100*[1]    | CANgw - res |             |
|                                             |     1804     |       resButtons        |   sensor   |   1/3/5/7*[1]   | CANgw - res |             |
|                                             |     2113     |       steerFault        |   sensor   |      bool       | StateM      |             |
|                                             |     2114     |        ebsState         |   sensor   |     0-2*[2]     | StateM      |             |
|                                             |     2115     |      serviceValve       |   sensor   |      bool       | StateM      |             |
|                                             |     1049     |          ebsOk          |   sensor   |      bool       | ASNode      |             |
|                                             |     1112     |      clampExtended      |   sensor   |      bool       | ASNode      |             |
|                                             |     1115     |          asms           |   sensor   |      bool       | ASNode      |             |
|                                             |   (unset)    |       tsActivated       |   sensor   |      bool       | ASNode      |             |
|                                             |     1916     |          KnobR          |   sensor   |    1-12 int     | CANgw-Lynx  |             |
|                                             |     1917     |          NnobL          |   sensor   |    1-12 int     | CANgw-Lynx  |             |
|                                             |     1917     |      missionState       |   sensor   |     0-4 int     | MissionCtrl |             |
|     opendlv::proxy::SwitchStateRequest      |     1044     |       ebsSpeaker        |    req     |      bool       | StateM      |             |
|                                             |     1027     |        heartBeat        |    req     |      bool       | StateM      |             |
|                                             |     1045     |       compressor        |    req     |      bool       | StateM      |             |
|                                             |     1066     |     finishedSignal      |    req     |      bool       | StateM      |             |
|                                             |     1067     |     shutdownSignal      |    req     |      bool       | StateM      |             |
|                                             |     1899     |      resInitialize      |    req     | Don't Care*[1]  | StateM      | CANgw-Res   |
|                                             |     1904     |     asReadyToDrive      |    req     |       1/0       | StateM      | CANgw-Lynx  |
|    opendlv::proxy::GroundSteeringReading    |     1200     |    steeringPosition     |   sensor   |       mm        | ASNode      |             |
|                                             |     1206     |      rackPosition       |   sensor   |       mm        | ASNode      |             |
|    opendlv::proxy::GroundSteeringRequest    |     2801     |     steeringRequest     |    req     |       deg       | aimPoint    | latCtrl     |
|     opendlv::proxy::GroundSpeedRequest      |     2201     |      speedRequest       |    req     |       m/s       | velPlan     | longCtrl    |
|       opendlv::proxy::PressureReading       |     1202     |     pressureService     |   sensor   |       bar       | ASNode      |             |
|                                             |     1205     |    pressureRegulator    |   sensor   |       bar       | ASNode      |             |
|                                             |     1201     |     pressureEBSLine     |   sensor   |       bar       | ASNode      |             |
|                                             |     1203     |     pressureEBSAct      |   sensor   |       bar       | ASNode      |             |
|                                             |     1509     |       brakeTarget       |   sensor   |                 | ?           |             |
| opendlv::proxy::PulseWidthModulationRequest |     2150     |     brakeDutyCycle      |    req     |   dutyCycles    | Brake       | StateM      |
|                                             |     1341     |     brakeDutyCycle      |    req     |   dutyCycles    | StateM      | ASNode      |
|                                             |     1300     |     blueAssiSignal      |    req     |   dutyCycles    | StateM      | ASNode      |
|                                             |     1320     |      redAssiSignal      |    req     |   dutyCycles    | StateM      | ASNode      |
|                                             |     1321     |     greenAssiSignal     |    req     |   dutyCycles    | StateM      | ASNode      |
|                                             |     1340     |    steeringDutyCycle    |    req     |   dutyCycles    | latCtrl     | ASNode      |
|   opendlv::proxy::AngularVelocityReading    |     112      |     angularVelocity     |   sensor   |      rad/s      | imu         |             |
|     opendlv::proxy::AccelerationReading     |     112      |      acceleration       |   sensor   |      m/s^2      | imu         |             |
|    opendlv::proxy::GeodeticWgs84Reading     |     112      |       geolocation       |   sensor   |       deg       | imu (gps)   |             |
|     opendlv::proxy::GroundSpeedReading      |     112      |       groundSpeed       |   sensor   |       m/s       | imu (gps)   |             |
|                                             |     113      |       groundSpeed       |   sensor   |       m/s       | SLAM (ekf)   |             |
|                                             |     2500     |       groundSpeed       |   sensor   |       m/s       | SLAM         |             |
|                                             |     3000     |       groundSpeed       |   sensor   |       m/s       | speedEst    |             |
|             opendlv::sim::Frame             |     113      |       eulerAngle        |   sensor   |       deg       | imu (ekf)   |             |
|    opendlv::logic::sensation::Geolocation   |     113      |       geolocation       |   sensor   |       deg       | imu (ekf)   |             |
|        opendlv::sim::KinematicState         |     2501     |        velocity         |   sensor   |       m/s       | SLAM        |             |
|             opendlv::sim::Frame             |     2501     |          pose           |   sensor   |    m,degree     | SLAM        |             |
|  opendlv.logic.perception.ObjectFrameStart  |              |                         |            |                 |             |             |
|   opendlv.logic.perception.ObjectFrameEnd   |              |                         |            |                 |             |             |
|       opendlv.logic.perception.Object       |              |                         |            |                 |             |             |
|     opendlv.logic.perception.ObjectType     |              |                         |            |                 |             |             |
|   opendlv.logic.perception.ObjectPosition   |              |                         |            |                 |             |             |
|  opendlv.logic.sensation.Equilibrioception  |              |                         |            |                 |             |             |
|       opendlv.logic.action.LocalPath        |     2601     |          path           |            |                 | pathPlanner |             |
|        opendlv::proxy::TorqueRequest        |     2102     |       torqueLeft        |    req     |    0~2400cNm    | longCtrl    |             |
|                                             |     2103     |       torqueRight       |    req     |    0~2400cNm    | longCtrl    |             |
|        opendlv::proxy::TorqueReading        |     1932     |  torqueEstimationRight  |   sensor   |       cNm       | CANgw-Lynx  |             |
|                                             |     1934     |  torqueEstimationLeft   |   sensor   |       cNm       | CANgw-Lynx  |             |
|         opendlv::system::LogMessage         |     1930     |      ErrorRightPE       |   logmsg   |                 | CANgw-Lynx  |             |
|                                             |     1931     |       ErrorLeftPE       |   logmsg   |                 | CANgw-Lynx  |             |

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
| logic    | StateMachine        | 2100   |
|          | longCtrl            | 2200   |
|          | Brake               | 2300   |
|          | velPlan             | 2400   |
|          | SLAM                | 2500   |
|          | pathPlan            | 2600   |
|          | aimPoint            | 2700   |
|          | latCtrl             | 2800   |
|          | MissionCtrl         | 2900   |
|          | Speed estimation    | 3000   |
