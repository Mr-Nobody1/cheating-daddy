<img width="1299" height="424" alt="cd (1)" src="https://github.com/user-attachments/assets/b25fff4d-043d-4f38-9985-f832ae0d0f6e" />

## Recall.ai - API for desktop recording

If you're looking for a hosted desktop recording API, consider checking out [Recall.ai](https://www.recall.ai/product/desktop-recording-sdk/?utm_source=github&utm_medium=sponsorship&utm_campaign=sohzm-cheating-daddy), an API that records Zoom, Google Meet, Microsoft Teams, in-person meetings, and more.

This project is sponsored by Recall.ai.

---

> [!NOTE]  
> Use latest MacOS and Windows version, older versions have limited support

> [!NOTE]  
> During testing it wont answer if you ask something, you need to simulate interviewer asking question, which it will answer

A real-time AI assistant that provides contextual help during video calls, interviews, presentations, and meetings using screen capture and audio analysis.

## Features

- **Live AI Assistance**: Real-time help powered by Google Gemini 2.5 Flash
- **Screen & Audio Capture**: Analyzes what you see and hear for contextual responses
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
2. Choose your profile and language in settings
3. Configure response quality settings (verbosity, code detail level, render mode)
4. Click "Start Session" to begin
5. Position the window using keyboard shortcuts
6. The AI will provide real-time assistance based on your screen and what interview asks

## Response Quality Settings

Access via **Settings → Response Quality**:

- **Response Verbosity**: Concise (1-3 sentences), Balanced (3-6 sentences), or Detailed (comprehensive)
- **Code Detail Level**: Logic Only (pseudocode), Key Snippets, or Complete Code
- **Include Examples**: Toggle example inputs/outputs for code solutions
- **Render Mode**: Streaming (progressive display) or Batch (complete response at once)

> Note: Verbosity and code detail settings require starting a new session to take effect.

## Keyboard Shortcuts

- **Window Movement**: `Ctrl/Cmd + Arrow Keys` - Move window
- **Click-through**: `Ctrl/Cmd + M` - Toggle mouse events
- **Close/Back**: `Ctrl/Cmd + \` - Close window or go back
- **Send Message**: `Enter` - Send text to AI
- **Next Step**: `Ctrl/Cmd + Enter` - Take screenshot and ask for next step
- **Navigate Responses**: `Ctrl/Cmd + [` / `]` - Previous/Next response
- **Scroll Response**: `Ctrl/Cmd + Shift + Up/Down` - Scroll content

## Audio Capture

- **macOS**: [SystemAudioDump](https://github.com/Mohammed-Yasin-Mulla/Sound) for system audio
- **Windows**: Loopback audio capture
- **Linux**: Microphone input

## Requirements

- Electron-compatible OS (macOS, Windows, Linux)
- Gemini API key
- Screen recording permissions
- Microphone/audio permissions
