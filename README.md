# MIDI Popup System

A retro Windows 95-style MIDI-reactive visual system that creates dynamic popup windows and terminal output based on real-time MIDI input. This system transforms your MIDI performance into an immersive audiovisual experience reminiscent of classic computing interfaces.

## Features

### 🎹 MIDI Reactivity
- **Real-time MIDI Input**: Responds to MIDI notes, control changes, and program changes
- **Multi-device Support**: Automatically detects and connects to all available MIDI input devices
- **Auto-reconnection**: Handles device disconnections and reconnections gracefully
- **MIDI Clock Filtering**: Ignores timing signals to focus on musical content

### 🖼️ Dynamic Popup System
- **8 Unique Popup Types**: Each MIDI note (60-67) creates different popup styles:
  - **Note 60**: Critical system error dialogs
  - **Note 61**: Progress bars and installation windows
  - **Note 62**: File save/load dialogs
  - **Note 63**: System input prompts
  - **Note 64**: Corrupted/glitched windows
  - **Note 65**: About/calculator dialogs
  - **Note 66**: Task manager/system monitor
  - **Note 67**: Network connection dialogs
- **Image Integration**: Random images from `pics/` folder (10,000+ available)
- **Colorful Variety**: 8 different color schemes rotate based on MIDI note values

### 🎛️ Three Positioning Modes
Control popup behavior via MIDI Program Change messages:
- **Program 0 (Centered)**: All popups stack in the center of the screen
- **Program 1 (Slight Random)**: Popups appear near center with subtle blur effects and 15% image chance
- **Program 2 (Fully Random)**: Complete chaos mode with 35% image chance and corrupted terminal output

### 💻 Retro Terminal Monitor
- **Real-time MIDI Monitoring**: Displays MIDI activity in a bash-style terminal
- **Chaos Mode**: In fully random mode, terminal output becomes corrupted with Unicode symbols
- **Command Variety**: Normal vs. unhinged command sets for different modes
- **Scrolling History**: Maintains terminal line history with automatic cleanup

### 🎨 Visual Effects
- **Velocity Sensitivity**: Popup intensity scales with MIDI note velocity
- **Blur Effects**: Dreamlike blur in slight random mode
- **Color Cycling**: Different color schemes for different notes
- **Chaos Styling**: Special visual corruption in fully random mode
- **Smooth Animations**: Fade in/out transitions and shake effects

### 🔧 Advanced Features
- **Auto-cleanup**: Popups clear after 2 seconds of MIDI inactivity
- **Memory Management**: Periodic cleanup prevents memory leaks
- **Screen Coverage Control**: Automatically removes oldest popups when screen gets crowded
- **MIDI CC Control**: 20+ control change mappings for real-time manipulation
- **Performance Optimization**: Optimized for low-latency response

## Quick Start

1. **Open the System**: Load `midi-popup.html` in a modern web browser
2. **Connect MIDI**: The system will automatically detect and connect to MIDI devices
3. **Start Playing**: 
   - Send MIDI notes 60-67 to create different popup types
   - Use Program Change 0/1/2 to switch positioning modes
   - Watch the terminal for real-time MIDI monitoring

## Controls

### Keyboard Shortcuts
- **Spacebar**: Clear all popups manually
- **Ctrl+C**: Clear terminal output
- **F11**: Force MIDI device reconnection
- **F12**: Toggle terminal visibility

### MIDI Program Changes
- **Program 0**: Centered stacking mode
- **Program 1**: Slight randomness with blur effects
- **Program 2**: Full chaos mode with corruption

### MIDI Control Changes
The system responds to various CC messages for real-time control:
- **CC 1 (Mod Wheel)**: Horizontal position
- **CC 2 (Breath)**: Vertical position  
- **CC 7 (Volume)**: Popup size
- **CC 10 (Pan)**: Rotation
- **CC 11-20**: Various color and style controls
- **CC 64-67**: Behavioral controls (sustain, portamento, etc.)

## Technical Requirements

- **Web Browser**: Modern browser with Web MIDI API support (Chrome, Edge, Opera)
- **MIDI Interface**: USB MIDI interface or virtual MIDI ports
- **Images** (Optional): Place JPG images in `pics/` folder for image popup mode

## File Structure

```
Webcore/
├── midi-popup.html          # Main application file
├── pics/                    # Image folder (10,000+ JPG files)
│   ├── 3.jpg
│   ├── 4.jpg
│   ├── ...
│   └── 999 (10).jpg
└── README.md               # This file
```

## Browser Compatibility

| Browser | Web MIDI Support | Status |
|---------|------------------|--------|
| Chrome  | ✅ Full         | Recommended |
| Edge    | ✅ Full         | Supported |
| Opera   | ✅ Full         | Supported |
| Firefox | ❌ No          | Not supported |
| Safari  | ❌ No          | Not supported |

## MIDI Note Mapping

| MIDI Note | Popup Type | Description |
|-----------|------------|-------------|
| 60 (C4)   | Critical Error | Red fatal system error dialogs |
| 61 (C#4)  | Progress Bar | Installation/loading windows |
| 62 (D4)   | File Dialog | Save/load file prompts |
| 63 (D#4)  | Input Dialog | System input/password prompts |
| 64 (E4)   | Corrupted | Glitched/corrupted windows |
| 65 (F4)   | Calculator | About/info dialogs |
| 66 (F#4)  | Task Manager | Process/system monitor |
| 67 (G4)   | Network | Connection/network dialogs |
| Other     | Default | Critical error (fallback) |

## Performance Tips

- **Reduce Image Frequency**: Lower image probabilities if experiencing lag
- **Monitor Popup Count**: System automatically manages popup density
- **Use Chaos Mode Sparingly**: Fully random mode is more CPU intensive
- **Clear Regularly**: Use spacebar to manually clear popups during long sessions

## Troubleshooting

### MIDI Not Working
1. Check browser MIDI support (Chrome recommended)
2. Ensure MIDI device is connected before loading page
3. Use F11 to force reconnection
4. Check browser console for error messages

### Performance Issues
1. Close other browser tabs
2. Reduce MIDI note velocity
3. Use Program 0 (centered mode) for better performance
4. Clear popups regularly with spacebar

### Images Not Loading
1. Ensure `pics/` folder exists in same directory
2. Check image file naming (3.jpg, 4.jpg, etc.)
3. Verify browser can access local files

## Advanced Usage

### Custom Images
Add your own images to the `pics/` folder following the naming convention:
- Base images: `3.jpg`, `4.jpg`, ..., `999.jpg`
- Variations: `3 (2).jpg`, `3 (3).jpg`, ..., `999 (10).jpg`

### MIDI Routing
For best results, route different drum/percussion sounds to notes 60-67 to get varied popup types. Use Program Change messages to switch between visual modes during performance.

### Integration
The system can be integrated into live performances, music production workflows, or art installations. The Web MIDI API allows connection to any MIDI software or hardware.

## License

This project is open source. Feel free to modify and adapt for your own creative projects.

## Credits

- Retro Windows 95 aesthetic inspiration
- Web MIDI API for real-time MIDI integration
- Unicode characters for chaos mode effects
- Modern web technologies for smooth performance
