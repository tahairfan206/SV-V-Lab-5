# Smart Museum Artifact Conservation System — Operations List

| OP_Id | Operation | Purpose |
|-------|-----------|---------|
| OP1 | PerformSelfCheck | To verify all essential sensors and environmental-control devices are working before allowing normal chamber operation. |
| OP2 | RecordArtifactData | To store the artifact's identification information when it is placed inside the chamber. |
| OP3 | LoadEnvironmentalProfile | To load the artifact's required environmental limits so the system can monitor against them. |
| OP4 | MonitorEnvironmentalConditions | To continuously compare actual temperature and humidity readings against the artifact's permitted range. |
| OP5 | CorrectTemperature | To restore temperature to the permitted range when it moves outside the artifact's limits. |
| OP6 | CorrectHumidity | To restore humidity to the permitted range when it moves outside the artifact's limits. |
| OP7 | VerifyRecovery | To confirm, through sensor readings, that a corrected condition has actually returned to the permitted range before resuming normal operation. |
| OP8 | ReduceLightExposure | To lower light exposure to the artifact as a protective measure during a protection response. |
| OP9 | ActivateAdditionalControls | To engage extra environmental-control devices to protect the artifact during a protection response. |
| OP10 | GenerateOperatorAlert | To notify the museum operator that the system has entered protection mode. |
| OP11 | DetectVibration | To sense and evaluate vibration levels against the permitted threshold. |
| OP12 | SuspendRiskyActivities | To halt activities that could increase risk to the artifact when significant vibration is detected. |
| OP13 | VerifyVibrationStability | To confirm vibration has remained below the threshold for the full stabilization period before resuming normal conservation. |
| OP14 | SuspendConservationOnDoorOpen | To immediately halt normal conservation activity when the chamber door is opened. |
| OP15 | VerifyConditionsBeforeResume | To re-check the artifact's environmental conditions and sensor status before resuming conservation after the door is closed again. |
| OP16 | SwitchToEmergencyPower | To transfer the chamber to an emergency power source when main power is lost. |
| OP17 | RecordIncident | To log the event when power is lost and no emergency power source is available. |
| OP18 | PerformSafeShutdown | To bring the system into a safe shutdown state when emergency power is unavailable. |
| OP19 | ConfirmSafeRemovalCondition | To verify the chamber is in a safe condition with no active protection response before allowing artifact removal. |
