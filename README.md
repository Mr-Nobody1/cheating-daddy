<img width="1299" height="424" alt="betterly" src="src/assets/gemini.png" />

---

> [!NOTE]  
> Use latest MacOS and Windows version, older versions have limited support

> [!NOTE]  
> During testing it wont answer if you ask something, you need to simulate interviewer asking question, which it will answer

A real-time AI assistant that provides contextual help during video calls, interviews, presentations, and meetings using screen capture and audio analysis.

## Features

- **Live AI Assistance**: Real-time help powered by Google Gemini 2.5 (Flash or Pro) with Gemini 3 Pro Preview for vision
- **Model Selection**: Choose between Gemini 2.5 Flash (free, 20/day) or Pro (paid, unlimited)
- **Screen & Audio Capture**: Analyzes what you see and hear for contextual responses
- **Multi-screenshot Batching**: Queue `S1`, `S2`, `S3`... and send them together as one prompt/request
- **Multiple Profiles**: Interview, Sales Call, Business Meeting, Presentation, Negotiation, Exam
- **Response Quality Settings**: Configure verbosity (Concise/Balanced/Detailed) and code detail level
- **Render Mode**: Choose between streaming or batch response display
- **Text Chat**: Send typed messages with fast HTTP API fallback
- **Transparent Overlay**: Always-on-top window that can be positioned anywhere
- **Click-through Mode**: Make window transparent to clicks when needed
- **Cross-platform**: Works on macOS, Windows, and Linux (kinda, dont use, just for testing rn)

## Setup

1. **Get a Gemini API Key**: Visit [Google AI Studio](https://aistudio.google.com/apikey)
2. **Install Dependencies**: `npm install` or `bun install`
3. **Run the App**: `npm start` or `bun start`

## Usage

1. Enter your Gemini API key in the main window
2. Choose your AI model (Flash or Pro) in Settings → Model
3. Choose your profile and language in settings
4. Configure response quality settings (verbosity, code detail level, render mode)
5. Click "Start Session" to begin
6. Position the window using keyboard shortcuts
7. Press `Ctrl/Cmd + Shift + S` to queue screenshots (`S1`, `S2`, ...)
8. Press `Ctrl/Cmd + Shift + D` to send the queued screenshots as one single prompt/request
9. The AI will provide real-time assistance based on your screen and what interview asks

## Model Settings

Access via **Settings → Model**:

- **Gemini 2.5 Flash** (Default)
  - Free tier: 20 sessions per day
  - Fast, optimized for speed
  - Best for most use cases

- **Gemini 2.5 Pro**
  - Requires paid API key
  - Unlimited sessions
  - Most capable model for complex scenarios

> Note: Model changes require starting a new session to take effect.

## Response Quality Settings

Access via **Settings → Response Quality**:

- **Response Verbosity**: Concise (1-3 sentences), Balanced (3-6 sentences), or Detailed (comprehensive)
- **Code Detail Level**: Logic Only (pseudocode), Key Snippets, or Complete Code
- **Include Examples**: Toggle example inputs/outputs for code solutions
- **Render Mode**: Streaming (progressive display) or Batch (complete response at once)

> Note: Verbosity and code detail settings are applied instantly during an active session.

## Keyboard Shortcuts

- **Window Movement**: `Ctrl/Cmd + Arrow Keys` - Move window
- **Click-through**: `Ctrl/Cmd + M` - Toggle mouse events
- **Close/Back**: `Ctrl/Cmd + \` - Close window or go back
- **Send Message**: `Enter` - Send text to AI
- **Next Step**: `Ctrl/Cmd + Enter` - Take screenshot and ask for next step
- **Queue Screenshot (Batch)**: `Ctrl/Cmd + Shift + S` - Capture screenshot into queue (`S1`, `S2`, ...)
- **Send Screenshot Batch**: `Ctrl/Cmd + Shift + D` - Send queued screenshots as one single prompt/request
- **Navigate Responses**: `Ctrl/Cmd + [` / `]` - Previous/Next response
- **Scroll Response**: `Ctrl/Cmd + Shift + Up/Down` - Scroll content

## Multi-Screenshot Flow

1. Start a live session
2. Press `Ctrl/Cmd + Shift + S` for each screenshot you want to queue
3. Watch the assistant status for `S1`, `S2`, `S3` capture progress
4. Press `Ctrl/Cmd + Shift + D` to send the full queue
5. The app submits the batch as a single model request and returns one combined answer

## Audio Capture

- **macOS**: [SystemAudioDump](https://github.com/Mohammed-Yasin-Mulla/Sound) for system audio
- **Windows**: Loopback audio capture
- **Linux**: Microphone input

## Requirements

- Electron-compatible OS (macOS, Windows, Linux)
- Gemini API key
- Screen recording permissions
- Microphone/audio permissions
