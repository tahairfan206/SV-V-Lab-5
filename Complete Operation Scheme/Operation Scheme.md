# Smart Museum Artifact Conservation System — Operation Schema

| Id | Pre_condition | Events/Inputs | Post_condition |
|----|----------------|-----------------|------------------|
| OP1 | Chamber powered on; sensors and environmental-control devices present | Power-on signal | All essential sensors report OK → system permitted to enter MONITORING mode; OR any essential sensor fails → system remains blocked from entering MONITORING mode |
| OP2 | Chamber in MONITORING mode | Artifact placed inside chamber | Artifact ID and required environmental limits stored by the system |
| OP3 | Artifact data (ID + limits) recorded | Artifact data available | Environmental profile becomes active and usable for comparison |
| OP4 | Sensors operational; artifact present | Continuous sensor readings (temperature, humidity) | Actual readings compared against loaded environmental profile limits |
| OP5 | CONSERVATION_ACTIVE mode; environmental profile loaded | Temperature detected outside permitted range | Environmental-control mechanism activated to restore temperature |
| OP6 | CONSERVATION_ACTIVE mode; environmental profile loaded | Humidity detected outside permitted range | Environmental-control mechanism activated to restore humidity |
| OP7 | Correction command issued (OP5 or OP6) in progress | Sensor readings during recovery period | Condition confirmed back within range → normal operation resumes; OR recovery period expires without success → PROTECTION_MODE triggered |
| OP8 | System has entered PROTECTION_MODE | Protection response activated | Light exposure to the artifact reduced |
| OP9 | System has entered PROTECTION_MODE | Protection response activated | Additional environmental-control devices engaged |
| OP10 | System has entered PROTECTION_MODE | Protection response activated | Alert delivered to museum operator |
| OP11 | Vibration sensor operational; artifact present | Continuous vibration readings | Vibration level compared against permitted threshold |
| OP12 | Artifact inside chamber | Significant vibration detected (OP11) | Risk-increasing activities halted; system enters VIBRATION_RESPONSE |
| OP13 | System in VIBRATION_RESPONSE | Vibration level observed below threshold | Vibration confirmed below threshold for full stabilization period → normal conservation may resume; OR period not yet satisfied → system remains in VIBRATION_RESPONSE |
| OP14 | CONSERVATION_ACTIVE mode | Chamber door opens | Normal conservation activity immediately suspended |
| OP15 | Conservation was suspended (OP14) | Chamber door closed again | Environmental conditions and sensor status verified → CONSERVATION_ACTIVE resumes only if verification passes; otherwise operation remains suspended |
| OP16 | Conservation in progress; emergency power source available | Power loss detected | System switches to emergency power; conservation continues |
| OP17 | Power loss detected; emergency power source unavailable | Power loss event | Incident logged with timestamp |
| OP18 | Incident recorded (OP17) | No emergency power available | System enters safe shutdown state |
| OP19 | Operator requests artifact removal | Removal request event | Chamber confirmed safe with no active protection response → removal permitted; otherwise removal blocked |
