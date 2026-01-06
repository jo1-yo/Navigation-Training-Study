# Logging Schema (Data Dictionary)

This document defines the event- and sensor-level logs exported by the study app.

## Core Identifiers
- `participant_id` (string): anonymized ID (do not store real names)
- `session_id` (string): unique session identifier
- `study_code` (string): researcher-provided code that gates access
- `trial_id` (string/int): trial index within a session
- `condition` (string): experimental condition label

## Event Log (recommended fields)
Each row/event should include:
- `timestamp_ms` (int): Unix timestamp in milliseconds or ms since session start
- `event_type` (string): e.g., `session_start`, `trial_start`, `response`, `trial_end`, `session_end`
- `event_value` (string/number, optional): e.g., response choice, error code
- `metadata` (json, optional): device info, screen size, etc.

## Sensor Log (if using device orientation)
- `timestamp_ms` (int)
- `alpha` (float, optional)
- `beta` (float, optional)
- `gamma` (float, optional)
- `sampling_hz` (float, optional): expected sampling rate

## Export Formats
- CSV: one file for events and one file for sensors (recommended)
- JSON: hierarchical session object with events/sensors arrays

## Notes
- Do NOT commit real participant data.
- Use synthetic exports for examples in `sample_data/`.
