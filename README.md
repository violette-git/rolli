# ROLI Seaboard Web Emulator

A web-based emulation of the ROLI Seaboard's innovative touch-sensitive keyboard interface, providing an expressive musical experience directly in your browser.

## Table of Contents
- [Quick Start](#quick-start)
- [Project Overview](#project-overview)
- [Features](#features)
- [5D Touch Interactions](#5d-touch-interactions)
- [User Guide](#user-guide)
  - [Getting Started](#getting-started)
  - [Playing the Instrument](#playing-the-instrument)
  - [Sound Controls](#sound-controls)
  - [Recording](#recording)
- [Technical Implementation](#technical-implementation)
  - [Web Technologies](#web-technologies)
  - [Audio Synthesis](#audio-synthesis)
  - [Touch Interaction](#touch-interaction)
- [Browser and Device Compatibility](#browser-and-device-compatibility)
- [Installation](#installation)
- [Troubleshooting](#troubleshooting)

## Quick Start

1. Open [landing.html](landing.html) in a modern web browser (Chrome recommended)
2. Choose between the original or enhanced version of the application
3. Click anywhere on the page to initialize audio
4. Play the keyboard using mouse or touch:
   - Click/tap for basic notes
   - Press and hold for pressure sensitivity
   - Slide horizontally for pitch bending
   - Slide vertically for timbre changes

## Project Overview

The ROLI Seaboard Web Emulator recreates the innovative touch-sensitive keyboard experience of the ROLI Seaboard hardware in a web browser. This project aims to provide musicians and enthusiasts with an accessible way to explore the expressive capabilities of the Seaboard's unique interface without requiring specialized hardware.

The application uses modern web technologies to simulate the Seaboard's distinctive "5D Touch" system, allowing for nuanced musical expression through various touch interactions.

## Features

- **5D Touch Emulation**: Simulates the five dimensions of touch that make the ROLI Seaboard unique
- **Polyphonic Synthesizer**: Play multiple notes simultaneously with independent expression
- **Sound Customization**: Choose from multiple oscillator types and adjust sound parameters
- **Audio Effects**: Apply reverb and delay effects to enhance your sound
- **Recording Capability**: Record your performances and export as audio files
- **Responsive Design**: Works across desktop and mobile devices
- **Multi-Touch Support**: Use multiple fingers simultaneously on touch-enabled devices

## 5D Touch Interactions

The ROLI Seaboard is known for its "5D Touch" system, which this web emulator recreates:

1. **Strike**: The initial velocity of your touch determines the volume of the note
2. **Press**: Continuous pressure after the initial touch controls sound intensity
3. **Glide**: Horizontal movement between notes creates smooth pitch transitions
4. **Slide**: Vertical movement on a note changes timbre or other sound characteristics
5. **Lift**: How you release a note affects its decay characteristics

```
┌─────────────────────────────────────────────────────┐
│                                                     │
│  STRIKE  →  PRESS  →  GLIDE  →  SLIDE  →  LIFT     │
│  (touch)   (depth)   (horiz)   (vert)    (release) │
│                                                     │
└─────────────────────────────────────────────────────┘
```

## User Guide

### Getting Started

1. **Launch the Application**: Open either version of the application in your web browser
   - Original version: [index.html](index.html)
   - Enhanced version: [index_enhanced.html](index_enhanced.html)

2. **Initialize Audio**: Click anywhere on the page when prompted to initialize the Web Audio API

3. **Interface Overview**:
   - The keyboard interface appears as a dark surface with key indicators
   - Control panels provide access to sound parameters and recording functions

### Playing the Instrument

The keyboard can be played using either mouse or touch interactions:

- **Basic Note Playing**:
  - Click or tap on a key to play a note
  - The velocity of your click/tap affects the initial volume

- **Expressive Playing**:
  - Press and hold to control sound intensity with pressure
  - Slide horizontally while holding to bend pitch between notes
  - Move vertically on a key to modify timbre
  - Use multiple fingers on touch devices for polyphonic expression

- **Tips for Expressive Playing**:
  - Start with light touches to understand the pressure sensitivity
  - Practice slow glides between notes for smooth transitions
  - Experiment with vertical movements to discover timbre variations

### Sound Controls

The application provides several controls to customize your sound:

- **Oscillator Type**: Choose between sine, square, triangle, and sawtooth waveforms
- **Attack/Release**: Adjust how quickly notes begin and end
- **Effects**: Control reverb and delay amounts
- **Master Volume**: Adjust the overall output level

### Recording

To record your performance:

1. Click the "Start Recording" button
2. Play your performance
3. Click "Stop Recording" when finished
4. Use the "Save Recording" button to download your performance as a WAV file

## Technical Implementation

### Web Technologies

The ROLI Seaboard Web Emulator is built using the following technologies:

- **HTML5**: Structure and user interface elements
- **CSS3**: Styling and responsive design
- **JavaScript**: Core application logic and user interaction
- **Canvas API**: Rendering the keyboard interface
- **Web Audio API**: Audio synthesis and processing
- **Tone.js**: High-level audio framework for synthesizer implementation

### Audio Synthesis

The application uses Tone.js and the Web Audio API to create a polyphonic synthesizer with the following components:

- **Tone.PolySynth**: Handles multiple simultaneous notes
- **Oscillators**: Generate the basic sound waveforms
- **Envelopes**: Shape the amplitude of each note over time
- **Effects**: Process the audio with reverb and delay
- **Pressure Mapping**: Translates touch/mouse input to sound parameters

Example of the synthesizer initialization:

```javascript
const synth = new Tone.PolySynth(Tone.Synth).toDestination();
synth.set({
  oscillator: {
    type: "sine"
  },
  envelope: {
    attack: 0.1,
    decay: 0.2,
    sustain: 0.8,
    release: 1.5
  }
});
```

### Touch Interaction

The application captures and processes touch interactions using:

- **Touch Events API**: Detects multi-touch interactions on touch-enabled devices
- **Mouse Events**: Provides fallback for non-touch devices
- **Pressure Mapping**: Simulates pressure sensitivity using various input parameters
- **Event Handling**: Processes complex gestures and continuous interactions

## Browser and Device Compatibility

The ROLI Seaboard Web Emulator works best on:

- **Desktop Browsers**:
  - Chrome (recommended for best performance)
  - Firefox
  - Edge
  - Safari

- **Mobile Devices**:
  - Modern iOS devices (iPhone, iPad) using Safari
  - Android devices using Chrome

**Note**: Touch sensitivity features work best on devices with pressure-sensitive screens. On devices without pressure sensitivity, the application simulates pressure based on touch duration and movement.

## Installation

No installation is required. Simply download the project files and open the HTML files in a compatible web browser:

1. Download all project files to a local directory
2. Open landing.html, index.html, or index_enhanced.html directly in your browser
3. Alternatively, host the files on a web server for online access

## Troubleshooting

| Issue | Solution |
|-------|----------|
| No sound | Click anywhere on the page to initialize audio. Check that your device volume is turned up. |
| Laggy performance | Close other browser tabs and applications. Try using Chrome for best performance. |
| Touch not working | Ensure you're using a touch-enabled device. Try the mouse interface as an alternative. |
| Recording issues | Make sure you've granted microphone permissions if prompted. Try shorter recordings if experiencing memory issues. |
| Pressure sensitivity not working | Not all devices support pressure sensitivity. The application will simulate pressure based on touch duration. |

If you encounter persistent issues, try:
1. Refreshing the page
2. Clearing browser cache
3. Using a different browser
4. Updating your browser to the latest version