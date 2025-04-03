# ROLI Seaboard Web Emulator - User Guide

## Introduction

The ROLI Seaboard Web Emulator is a browser-based application that simulates the innovative ROLI Seaboard MIDI controller. This web application allows you to experience the expressive capabilities of the ROLI Seaboard's unique touch-sensitive surface directly in your web browser.

## Getting Started

1. **Launch the Application**: Open the index.html file in a modern web browser.

2. **Start Audio**: Click the "Start Audio" button to initialize the Web Audio API. This step is necessary due to browser security policies that require user interaction before audio can play.

3. **Play the Keyboard**: The main interface displays a keyboard-like surface that responds to your touch or mouse interactions.

## 5D Touch Interactions

The ROLI Seaboard is known for its "5D Touch" technology, which the web emulator simulates through the following dimensions:

### 1. Strike
- **How to use**: Tap or click on a key to initiate a note.
- **Effect**: The initial velocity of your tap/click determines the initial volume of the note.
- **Tips**: Experiment with different striking forces to create dynamic expression.

### 2. Press
- **How to use**: After striking a key, apply varying pressure (on pressure-sensitive devices) or use vertical mouse movement to simulate pressure changes.
- **Effect**: Modulates the sound's intensity and timbre.
- **Tips**: On non-pressure-sensitive devices, the vertical position of your finger/cursor on a key simulates pressure.

### 3. Glide
- **How to use**: Move your finger/cursor horizontally across the surface from one note to another.
- **Effect**: Creates a smooth pitch transition between notes (similar to a pitch bend).
- **Tips**: Try gliding between notes that are far apart to create dramatic pitch slides.

### 4. Slide
- **How to use**: Move your finger/cursor vertically on a key.
- **Effect**: Modifies the timbre/character of the sound.
- **Tips**: Combine with pressure for more expressive control.

### 5. Lift
- **How to use**: Release the key with varying speeds.
- **Effect**: Affects how the note fades out.
- **Tips**: Quick lifts create abrupt endings, while slow lifts allow for gentle fades.

## Sound Controls

### Oscillator Type
Select from various waveform types to change the basic sound character:
- Sine: Pure, smooth tone
- Triangle: Slightly richer than sine, still smooth
- Sawtooth: Bright, buzzy sound
- Square: Hollow, wind-instrument-like sound
- FM variants: More complex, modulated versions of the basic waveforms

### Effects

#### Reverb
- Adjusts the amount of simulated room ambience.
- Higher values create a larger, more spacious sound.

#### Delay
- Controls echo repetitions.
- Higher values create more pronounced echo effects.

#### Pressure Sensitivity
- Determines how responsive the instrument is to pressure/vertical movement.
- Higher values make the pressure dimension more pronounced.

## Recording Your Performance

1. Click the "Record" button to start recording your performance.
2. Play the Seaboard as desired.
3. Click "Stop Recording" when finished.
4. Click "Download Recording" to save your performance as an audio file.

## Multi-Touch Support

The web emulator supports playing multiple notes simultaneously:
- On touch devices: Use multiple fingers to play chords and complex passages.
- With mouse: The application can only track one pointer at a time.

## Browser and Device Compatibility

### Recommended Browsers
- Chrome (latest version)
- Firefox (latest version)
- Edge (latest version)
- Safari (latest version)

### Device-Specific Features
- **Touch Devices**: Best experience on tablets and touchscreen laptops that support pressure sensitivity (e.g., iPad Pro with Apple Pencil, Microsoft Surface with Surface Pen).
- **Desktop/Laptop**: Use mouse movement to simulate pressure and sliding.
- **Mobile Phones**: Functional but limited by screen size.

## Troubleshooting

### No Sound
- Ensure you've clicked the "Start Audio" button.
- Check that your device's volume is turned up.
- Verify that your browser allows audio playback.

### Performance Issues
- Close other browser tabs and applications to free up system resources.
- Reduce the reverb and delay settings if experiencing audio glitches.
- On mobile devices, use the device in landscape orientation for better keyboard access.

### Touch Response Problems
- Different devices have varying levels of touch sensitivity. Adjust the Pressure Sensitivity control to match your device's capabilities.
- Some older browsers may not fully support all touch features. Use the latest browser version when possible.

## Tips for Expressive Playing

1. **Combine Dimensions**: The true expressivity comes from using multiple dimensions simultaneously (e.g., gliding while changing pressure).

2. **Start Simple**: Begin by mastering one dimension at a time before combining them.

3. **Explore Sound Design**: Different oscillator types respond uniquely to the 5D touch interactions. Experiment to find interesting combinations.

4. **Record Your Experiments**: Use the recording feature to capture your most interesting performances and techniques.