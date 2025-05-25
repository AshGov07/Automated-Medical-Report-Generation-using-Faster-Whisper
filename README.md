# Automated Medical Report Generation using Faster Whisper

A Python-based voice-controlled medical transcription system specifically designed for first trimester gynecology reports. This application combines real-time speech recognition with automated document generation to streamline medical reporting workflows.

![Python](https://img.shields.io/badge/python-v3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

## 🎯 Features

### Core Functionality
- **Real-time Speech-to-Text**: Powered by OpenAI's Whisper model for accurate medical transcription
- **Voice Commands**: Navigate between report sections using natural language commands
- **Automated Document Generation**: Creates professional Word documents with proper formatting
- **Audio Recording**: Saves audio files alongside transcriptions for record-keeping
- **Multi-threaded Processing**: Handles recording and transcription simultaneously

### Medical Report Structure
Pre-configured for first trimester gynecology reports with sections including:
- Patient Information
- LMP (Last Menstrual Period)
- Gestational Age
- Type of Scan
- Uterine Position
- Endometrial Thickness
- Fetal Pole & Crown Rump Length
- Fetal Heart Rate
- Amniotic Fluid & Placental Position
- And more...

### User Interface
- **Intuitive GUI**: Built with Tkinter for cross-platform compatibility
- **Section Navigation**: Easy switching between report sections
- **Real-time Feedback**: Live transcription log and status updates
- **Content Management**: View and edit section content in real-time

## 🛠️ Installation

### Prerequisites
- Python 3.8 or higher
- Windows/macOS/Linux compatible
- Microphone access

### Required Dependencies
```bash
pip install -r requirements.txt
```

**Core Dependencies:**
```
tkinter
pyaudio
python-docx
RealtimeSTT
whisper
wave
threading
```

### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/AshGov07/Automated-Medical-Report-Generation-using-Faster-Whisper.git
   cd Automated-Medical-Report-Generation-using-Faster-Whisper
   ```

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Install System Audio Dependencies**
   
   **Windows:**
   ```bash
   pip install pyaudio
   ```
   
   **macOS:**
   ```bash
   brew install portaudio
   pip install pyaudio
   ```
   
   **Linux (Ubuntu/Debian):**
   ```bash
   sudo apt-get install python3-pyaudio
   ```

4. **Run the Application**
   ```bash
   python mycode4(final\ code).py
   ```

## 🚀 Usage

### Getting Started

1. **Launch the Application**
   - Run the Python script to open the GUI interface
   - The application will create a default save directory at `~/Desktop/wav files`

2. **Set Up Physician Information**
   - Enter the physician's name in the top field
   - Click "Update" to save to the document

3. **Begin Recording**
   - Select a report section from the left panel, or
   - Use voice command: "Go to [section name]"
   - Click "Start Recording" to begin transcription

### Voice Commands

The system recognizes various command patterns to navigate between sections:

```
"go to patient information"
"goto gestational age"  
"go to fetal heart rate"
```

**Supported Command Variations:**
- `go to [section]`
- `goto [section]`
- `go do [section]`
- `go 2 [section]`

### Workflow Example

1. Start the application
2. Say: "Go to patient information"
3. Dictate: "Patient is a 28-year-old female, gravida 2, para 1"
4. Say: "Go to gestational age"  
5. Dictate: "Based on LMP, gestational age is 8 weeks 3 days"
6. Continue through all sections...

## 📁 File Structure

```
├── mycode4(final code).py    # Main application file
├── requirements.txt          # Python dependencies
├── README.md                # This file
└── Desktop/wav files/       # Default output directory
    ├── First_Trimester_Report.docx
    └── recorded_audio.wav
```

## ⚙️ Configuration

### Audio Settings
The application uses optimized settings for medical transcription:
- **Model**: Whisper large-v2 for accuracy
- **Language**: English
- **Sensitivity**: Configured for clinical environments
- **Recording Format**: 44.1kHz, 16-bit WAV

### Customization Options
- Change save directory via File menu
- Modify report sections by editing the `headings` list
- Adjust transcription sensitivity in recorder configuration

## 🔧 Technical Details

### Architecture
- **Frontend**: Tkinter GUI with threaded operations
- **Speech Recognition**: RealtimeSTT with Whisper backend
- **Document Processing**: python-docx for Word document manipulation
- **Audio Processing**: PyAudio for real-time recording

### Key Components
- `GynecologyReportUI`: Main application class
- `AudioToTextRecorder`: Real-time transcription handler
- Command pattern matching for voice navigation
- Threaded buffer management for smooth operation

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues for:

- Additional medical report templates
- Enhanced voice command recognition
- UI/UX improvements
- Bug fixes and optimizations

### Development Setup
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📋 Requirements

### System Requirements
- **RAM**: Minimum 4GB (8GB recommended for optimal performance)
- **Storage**: 2GB free space for Whisper models
- **Audio**: Working microphone with clear input

### Python Dependencies
See `requirements.txt` for complete list of dependencies.

## 🐛 Troubleshooting

### Common Issues

1. **Audio Not Recording**
   - Check microphone permissions
   - Verify PyAudio installation
   - Test microphone in system settings

2. **Transcription Accuracy**
   - Speak clearly and at moderate pace
   - Ensure quiet environment
   - Check microphone positioning

3. **Document Not Saving**
   - Verify write permissions in save directory
   - Check available disk space
   - Ensure Word document isn't open in another application

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **AshGov07** - *Initial work* - [GitHub Profile](https://github.com/AshGov07)

## 🙏 Acknowledgments

- OpenAI for the Whisper speech recognition model
- RealtimeSTT library contributors
- Medical professionals who provided domain expertise
- Open source community for various supporting libraries

## 📞 Support

For support, please open an issue on GitHub or contact the maintainer through the GitHub profile.

---

**Note**: This application is designed to assist medical professionals in documentation. Always review and verify all transcribed content for accuracy before clinical use.
