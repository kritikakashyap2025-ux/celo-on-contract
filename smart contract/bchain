// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

/// @title Patient Vitals Record
/// @notice A simple contract to store and update patient vitals on-chain.
contract PatientVitals {

    // Struct to hold vital information
    struct Vitals {
        uint256 heartRate;      // beats per minute
        uint256 temperature;    // temperature in celsius * 10 (e.g., 375 = 37.5°C)
        uint256 bloodPressure;  // systolic value (for simplicity)
        uint256 lastUpdated;    // timestamp of last update
    }

    // Mapping from patient ID (address) to their vitals
    mapping(address => Vitals) private patientVitals;

    // Event for logging vital updates
    event VitalsUpdated(
        address indexed patient,
        uint256 heartRate,
        uint256 temperature,
        uint256 bloodPressure,
        uint256 timestamp
    );

    // Modifier to ensure only the patient can update their own vitals
    modifier onlyPatient(address _patient) {
        require(msg.sender == _patient, "Not authorized to update this record");
        _;
    }

    /// @notice Update your vitals
    /// @param _heartRate Patient's heart rate (bpm)
    /// @param _temperature Patient's body temperature (°C x10)
    /// @param _bloodPressure Patient's systolic blood pressure
    function updateVitals(
        uint256 _heartRate,
        uint256 _temperature,
        uint256 _bloodPressure
    ) external {
        patientVitals[msg.sender] = Vitals({
            heartRate: _heartRate,
            temperature: _temperature,
            bloodPressure: _bloodPressure,
            lastUpdated: block.timestamp
        });

        emit VitalsUpdated(msg.sender, _heartRate, _temperature, _bloodPressure, block.timestamp);
    }

    /// @notice Get the vitals for a specific patient
    /// @param _patient The address of the patient
    /// @return The patient's vitals
    function getVitals(address _patient) external view returns (Vitals memory) {
        return patientVitals[_patient];
    }
}
