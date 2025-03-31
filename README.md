# EEG_NIBS


🧠 Closed-Loop EEG & 4-Channel tACS/tDCS Neurostimulation System

Welcome to the documentation for a fully open-source, closed-loop EEG-integrated neurostimulation system, built entirely from scratch.

This repository contains the hardware designs, parts list, and firmware for a 4-channel tACS/tDCS stimulation system with real-time EEG integration, controlled via Python and Arduino Nano.

⸻

🧩 Project Overview

This system was developed to explore adaptive brain stimulation — modulating electrical currents based on real-time brain states, cognitive performance, or reinforcement learning algorithms.

Key Components:
	•	🧠 EEG Recording Module
	•	⚡ 4-Channel tDCS/tACS Stimulation Hardware
	•	🔁 Closed-Loop Python Control System
	•	🖥️ Arduino-based DAC current control
	•	🔐 Built-in Safety Features & Logging

The system is designed to serve researchers and developers interested in:
	•	Personalized neurostimulation
	•	Cognitive enhancement
	•	Reinforcement learning in neuroscience
	•	Brain-computer interfaces (BCIs)
	•	DIY neuroscience and open science hardware

⸻

🎯 Purpose

To provide a low-cost, flexible, and safe neurotechnology platform for:
	•	Closed-loop stimulation experiments
	•	Adaptive stimulation based on EEG/behavioral input
	•	Neuroscientific prototyping for brain state modulation
	•	Psychophysiological experiments

⸻

🛠️ Hardware Specifications

🔌 Stimulation Module (4-Channel tDCS/tACS)

Spec	Value/Feature
Channels	4 (individually addressable)
Max Current (per channel)	4 mA
Modulation Modes	tDCS, tACS (Sine, Square, Ramp, Custom)
Control Interface	Arduino Nano + DAC7311
Current Regulation	DAC-controlled + precision resistors
Voltage Reference	REF5050 or ADR5041 (5.0V)
Safety Features	Emergency analog cut-off, max current limit, resistance monitoring
Program Modes	5 fixed presets (2 x tDCS, 3 x tACS)
Control UI	1.3” OLED + 4 Buttons (Program, Start/Stop, ±Current)
Power Supply	Lab power (battery optional)



⸻

🧠 EEG Integration
	•	Interface for real-time EEG signal acquisition (designed for compatibility with OpenBCI or DIY amplifier)
	•	Real-time data streaming to Python
	•	Used to compute state, reward, and adaptation signals
	•	Clean switching logic to avoid interference during stimulation
	•	Log-based and adaptive session management

⸻

🧰 Bill of Materials (BoM)

(Full parts list available in parts_catalog.xlsx)

Example components:
	•	Arduino Nano (x4)
	•	DAC7311IDCKR (x2)
	•	TLC2252 Op-Amps (x4)
	•	REF5050 / ADR5041 Voltage Reference
	•	86.6Ω, 1.2kΩ, 2.2kΩ precision resistors
	•	1µF MLCC capacitors
	•	L78L05 voltage regulator
	•	SI8630BD Digital Isolator
	•	FMMT734/634 Darlington Transistors
	•	OLED 1.3” Display
	•	Tactile Buttons (x4)
	•	Toggle/Emergency Switch
	•	XL6009 Boost Converter

⸻

💻 Software / Firmware
	•	Arduino Sketches: arduino_code/
	•	Python Control Scripts (planned): python_control/
	•	EEG Integration & Analysis: eeg_pipeline/
	•	Safety & Log Scripts: logs/

⸻

🔄 Closed-Loop Flow
	1.	Cognitive Task → EEG + Task Performance Monitoring
	2.	Python Agent → Define State
	3.	RL Algorithm → Select Stimulation Protocol (Action)
	4.	Arduino Executes Program via DAC
	5.	EEG Feedback → Reward + Adaptation

⸻

📷 Visuals

PCB Layout, 3D Case Design, and Build Photos are included in assets/.

⸻

⚠️ Safety Notes
	•	Always monitor electrode resistance.
	•	Do not exceed 4 mA/channel.
	•	Use ramp-up/ramp-down transitions.
	•	Test with resistive dummy loads before skin contact.

⸻

👤 Author

Developed by Michael Roehrig, psychologist & AI enthusiast, diving into DIY neurotech to build accessible and intelligent brain interfaces.

Inspired by the incredible work of Prof. Roi Cohen Kadosh and open science communities.

⸻

📩 Contact & Collaboration

Interested in collaboration, replication, or feedback? Let’s connect via LinkedIn or GitHub issues!

⸻

📜 License

Open-source for research and educational use. Use responsibly. Not intended for clinical/medical use.

