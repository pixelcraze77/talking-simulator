# 🗣️ Python Talking Simulator

A simple real-time talking simulator written in Python.  
It switches between two images (idle & talking) based on microphone input,  
and adds subtle shaking animation while speaking.

This project uses **PyAudio**, **NumPy**, and **Pygame**.

---

## ✨ Features

- 🎤 **Voice detection** using RMS audio analysis  
- 🖼️ **Two-state character animation** (idle & talking)  
- 💥 **Talking shake effect** for more life-like motion  
- 🖱️ **Right-click menu**  
  - Change microphone device  
  - Change background color  
- 📊 **Automatic noise calibration** for reliable speech detection  
- 🧵 **Non-blocking audio thread** (UI stays smooth)

---

## 📦 Installation

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/python-talking-simulator.git
cd python-talking-simulator
````

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Program

Place your two transparent images in the project folder:

```
idle.png
talking.png
```

Then run:

```bash
python talking_simulator.py
```

---

## 📝 Requirements

The project requires the following Python libraries:

```text
pygame
pyaudio
numpy
tk
```

*(Automatically installed through `requirements.txt`.)*

---

## 📁 File Structure

```
├── talking_simulator.py      # Main program
├── idle.png                  # Idle image (transparent PNG)
├── talking.png               # Talking image (transparent PNG)
├── requirements.txt          # Dependencies
└── README.md                 # Documentation
```

---

## 🛠️ How It Works

### 🎤 Audio Processing

* Microphone audio is captured in a background thread
* RMS (volume level) is calculated every frame
* Automatic noise calibration sets a detection threshold
* When volume > threshold → talking mode

### 🖼️ Animation

* While talking:

  * The “talking” image is displayed
  * Small random shake is applied to create motion
* While silent:

  * The “idle” image is displayed

---

## 🖱️ Right-Click Menu

Right-click anywhere on the program window:

| Option | Description             |
| ------ | ----------------------- |
| **1**  | Change microphone       |
| **2**  | Change background color |

---

## 🧪 Example

Here is a picture of the program.

![talkingsimulator](talkingsimulator.png)

---

## 📜 License

This project is open-source under the MIT License.

---

## 🤝 Contributing

Pull requests are welcome!
Feel free to submit:

* bug fixes
* new features
* performance improvements
* UI enhancements

---

## ⭐ If You Like This Project…

Please give it a **star** on GitHub — it helps a lot!
