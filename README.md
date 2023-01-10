# Overview
Data Engineering Solution Submission for Hovanes Gasparian

## Description of the Data
Each entry (row) in the sample dataset gives the following features:
- `time`: The time the measurement was taken.
- `value`: The measured value corresponding to the sensor taking the reading.
- `field`: The field for the measured value. For encoders this indicates which cartesian coordinate the measurement is taken in (e.g. [`x`,`y`,`z`]) and for the `load_cell` (i.e. force measuring device) this gives the direction of the force vector in cartesian coordinates (e.g. [`fx`,`fy`,`fz`]).
- `robot_id`: The ID number for the robot being used (i.e. there are 2 robots so the `robot_id` is either `1` or `2`).
- `run_uuid`: A random ID number assigned to the part being formed.
- `sensor_type`: The type of sensor reporting data (e.g. encoder = robot position / load_cell = force measurements)

Note: The encoder gives all values in millimeters and the load cell gives all values in Newtons.

## Dependencies
Databricks runtime >= 11.2

## Instructions
See the run_instructions markdown page for integration with GitHub Actions
