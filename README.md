<div align="center">

# 🎬 ASCII Terminal Video Player

<img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=600&size=28&pause=1000&color=00FF00&center=true&vCenter=true&random=false&width=800&lines=Play+Videos+in+Your+Terminal+%F0%9F%96%A5%EF%B8%8F;ASCII+Art+Video+Player+%E2%9C%A8;Python+%7C+OpenCV+%7C+NumPy+%F0%9F%90%8D;Transform+Videos+into+ASCII+Art+%F0%9F%8E%A8;Terminal+Cinema+Experience+%F0%9F%8E%AD" alt="Typing SVG" />

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.7+-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/OpenCV-4.0+-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge" alt="Status"/>
</p>

<p align="center">
  <strong>Watch your favorite videos rendered as ASCII art directly in your terminal! A unique way to experience cinema in pure text form.</strong>
</p>

<p align="center">
  <i>"Why watch videos normally when you can watch them in ASCII? 🎥✨"</i>
</p>

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Demo](#-demo)
- [How It Works](#-how-it-works)
- [Tech Stack](#-tech-stack)
- [Installation](#-installation)
- [Usage](#-usage)
- [Configuration](#-configuration)
- [ASCII Character Set](#-ascii-character-set)
- [Performance Tips](#-performance-tips)
- [Troubleshooting](#-troubleshooting)
- [Examples](#-examples)
- [Advanced Usage](#-advanced-usage)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 Overview

**ASCII Terminal Video Player** is a Python-based application that converts video files into ASCII art and plays them directly in your terminal. Using computer vision and character mapping, it transforms each video frame into a text-based representation, creating a unique retro viewing experience.

Perfect for:
- 🎨 **Creative Projects** - Unique artistic video rendering
- 🖥️ **Terminal Enthusiasts** - Watch videos without leaving the terminal
- 📚 **Learning** - Understanding image processing and ASCII art
- 🎭 **Fun** - Impress your friends with terminal cinema!

### 💡 Why This Project?

- **Retro Aesthetic**: Experience videos in classic ASCII art style
- **Terminal Native**: No GUI needed, pure command-line experience
- **Lightweight**: Minimal resource usage compared to video players
- **Educational**: Learn computer vision, ASCII mapping, and frame processing
- **Customizable**: Adjust width, FPS, and character sets

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🎬 **Video Processing**
- ✅ Convert video frames to ASCII art
- ✅ Real-time frame rendering
- ✅ Automatic aspect ratio preservation
- ✅ Grayscale conversion
- ✅ Brightness-based character mapping
- ✅ Frame rate synchronization
- ✅ Support for multiple video formats

</td>
<td width="50%">

### ⚙️ **Customization**
- ✅ Adjustable output width (default: 80)
- ✅ Custom FPS control
- ✅ Configurable ASCII character set
- ✅ Frame limit option
- ✅ Keyboard interrupt support
- ✅ Cross-platform compatibility
- ✅ Clean terminal clearing

</td>
</tr>
<tr>
<td width="50%">

### 🎨 **ASCII Rendering**
- ✅ 10-character brightness gradient
- ✅ Smooth grayscale mapping
- ✅ Optimized for terminal display
- ✅ Maintains video proportions
- ✅ Character density based on brightness
- ✅ Dynamic frame resizing

</td>
<td width="50%">

### 🛠️ **Technical Features**
- ✅ OpenCV video processing
- ✅ NumPy array operations
- ✅ Error handling
- ✅ File validation
- ✅ Resource cleanup
- ✅ Efficient memory usage

</td>
</tr>
</table>

---

## 🎬 Demo

### Visual Examples

<div align="center">

### Original Video Frame vs ASCII Output

```
Original Frame                    ASCII Representation
┌─────────────┐                  ┌──────────────────────┐
│   🎬 Video  │       ───>       │  @@@@##**++--::.     │
│   Frame     │                  │  @@###***++--::.     │
│             │                  │  @##***++--::..      │
└─────────────┘                  │  #***++--::..        │
                                 │  **++--::..          │
                                 └──────────────────────┘
```

### ASCII Character Brightness Scale

```
Darkest ────────────────────────────> Brightest
  ' '     .    :    -    =    +    *    #    %    @
   │      │    │    │    │    │    │    │    │    │
   └──────┴────┴────┴────┴────┴────┴────┴────┴────┘
  Shadow  Dark Mid  Light  High  Very  Dense Full
          Tone Tone Tone   Mid   Bright Bright
```

### Sample ASCII Frame Output

```
                    @@@@@@@@@@@@@@
                @@@@############@@@@
              @@##****************##@@
            @@#***++++++======+++***##@@
          @@#**++==----------==++**###@@
        @@##*++==--::::::::--==++**###@@
      @@##**+==--::..........::--==+**##@@
    @@###*++==--::............::--=++**##@@
    @@##**+==--::.....    .....::--=+**###@@
    @@###*++=-::....        .....::-=+**##@@
      @@##**+=-::...        ...::-=+**##@@
        @@###*+=--::........::-=+**###@@
          @@###**+==----==++***###@@
            @@####**********####@@
              @@@@##########@@@@
                  @@@@@@@@@@
```

</div>

---

## 🧠 How It Works

### Processing Pipeline

```
┌──────────────┐
│ Video File   │
│  (MP4/AVI)   │
└──────┬───────┘
       │
       ▼
┌──────────────────────┐
│  OpenCV VideoCapture │
│  Read Frame-by-Frame │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│   Frame Resizing     │
│   (Maintain Ratio)   │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│  Grayscale Convert   │
│  (BGR to Gray)       │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│  Normalize (0-1)     │
│  Pixel Brightness    │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│  ASCII Mapping       │
│  Brightness → Char   │
└──────┬───────────────┘
       │
       ▼
┌──────────────────────┐
│  Terminal Display    │
│  Print ASCII Art     │
└──────────────────────┘
```

### 🔍 Technical Breakdown

#### **1. Frame Capture**
```python
cap = cv2.VideoCapture(video_path)
ret, frame = cap.read()
```
- Opens video file using OpenCV
- Reads frames sequentially
- Gets video FPS for timing

#### **2. Frame Resizing**
```python
height = int(frame.shape[0] * width / frame.shape[1] / 2)
resized_frame = cv2.resize(frame, (width, height))
```
- Calculates proportional height
- Divides by 2 for terminal aspect ratio
- Resizes to specified width

#### **3. Grayscale Conversion**
```python
gray_frame = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2GRAY)
```
- Converts color to grayscale
- Simplifies brightness analysis
- Reduces data to single channel

#### **4. Brightness Normalization**
```python
normalized = gray_frame / 255.0
```
- Scales pixel values to 0-1 range
- Prepares for character mapping
- Ensures consistent brightness levels

#### **5. ASCII Character Mapping**
```python
ascii_chars = " .:-=+*#%@"
index = int(pixel * (len(ascii_chars) - 1))
ascii_frame += ascii_chars[index]
```
- Maps normalized brightness to character index
- Darker pixels → spaces/dots
- Brighter pixels → hash/at symbols
- Creates ASCII string representation

#### **6. Terminal Display**
```python
print(ascii_art)
time.sleep(frame_delay)
```
- Prints ASCII frame to terminal
- Delays based on video FPS
- Maintains playback speed

---

## 🔥 Tech Stack

<div align="center">

### Core Technologies

<table>
<tr>
<td align="center" width="150">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="80" height="80" alt="Python" />
<br><strong>Python 3.7+</strong>
<br><sub>Core Language</sub>
</td>
<td align="center" width="150">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/opencv/opencv-original.svg" width="80" height="80" alt="OpenCV" />
<br><strong>OpenCV</strong>
<br><sub>Video Processing</sub>
</td>
<td align="center" width="150">
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" width="80" height="80" alt="NumPy" />
<br><strong>NumPy</strong>
<br><sub>Array Operations</sub>
</td>
</tr>
</table>

### Technologies Used

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)

### Libraries & Modules

- **cv2 (OpenCV)**: Video capture, frame processing, image manipulation
- **numpy**: Array operations, numerical computations
- **os**: File system operations, terminal clearing
- **time**: Frame rate timing, playback synchronization

</div>

---

## 🚀 Installation

### 📋 Prerequisites

- **Python 3.7 or higher**
- **pip** package manager
- **Terminal** with ASCII support

### ⚡ Quick Install

#### **Step 1: Clone the Repository**

```bash
git clone https://github.com/yourusername/ascii-terminal-video-player.git
cd ascii-terminal-video-player
```

#### **Step 2: Install Dependencies**

```bash
# Install required packages
pip install opencv-python numpy

# OR use requirements.txt
pip install -r requirements.txt
```

#### **Step 3: Add Your Video**

```bash
# Place your video file in the project directory
cp /path/to/your/video.mp4 ./video.mp4
```

#### **Step 4: Run the Player**

```bash
python ascii_video_player.py
```

### 📦 Requirements File

Create `requirements.txt`:

```txt
opencv-python>=4.5.0
numpy>=1.19.0
```

### 🐧 Platform-Specific Installation

#### **Ubuntu/Debian**
```bash
sudo apt-get update
sudo apt-get install python3-pip python3-opencv
pip3 install numpy
```

#### **macOS**
```bash
brew install python3
pip3 install opencv-python numpy
```

#### **Windows**
```bash
# Install Python from python.org
pip install opencv-python numpy
```

---

## 💻 Usage

### 🎯 Basic Usage

```bash
# Default settings (80 width, auto FPS)
python ascii_video_player.py
```

### ⚙️ Custom Configuration

Edit the parameters in the script:

```python
if __name__ == "__main__":
    video_path = "video.mp4"        # Your video file
    width = 80                      # Output width (characters)
    fps = 0                         # 0 = use video's original FPS
    
    play_video_in_terminal(video_path, width, fps)
```

### 🎬 Examples

#### **High Resolution Output**
```python
play_video_in_terminal("video.mp4", width=120, fps=30)
```

#### **Low Resolution (Faster)**
```python
play_video_in_terminal("video.mp4", width=40, fps=15)
```

#### **Custom FPS**
```python
play_video_in_terminal("video.mp4", width=80, fps=24)
```

### ⌨️ Keyboard Controls

| Key | Action |
|-----|--------|
| `Ctrl+C` | Stop playback |
| `q` | Quit (if implemented) |

---

## ⚙️ Configuration

### 🎨 ASCII Character Set

The default character set represents brightness levels:

```python
ascii_chars = " .:-=+*#%@"
```

**Brightness Scale:**
- `' '` (space) = Darkest (0% brightness)
- `.` = Very Dark (10%)
- `:` = Dark (20%)
- `-` = Mid-Dark (30%)
- `=` = Medium (40%)
- `+` = Mid-Light (50%)
- `*` = Light (60%)
- `#` = Bright (70%)
- `%` = Very Bright (80%)
- `@` = Brightest (90-100%)

### 🎛️ Custom Character Sets

Try different ASCII character sets:

```python
# High contrast
ascii_chars = " ░▒▓█"

# Detailed
ascii_chars = " .'`^\",:;Il!i><~+_-?][}{1)(|\\/tfjrxnuvczXYUJCLQ0OZmwqpdbkhao*#MW&8%B@$"

# Simple
ascii_chars = " .oO@"

# Block elements
ascii_chars = " ▁▂▃▄▅▆▇█"

# Emoji-based (experimental)
ascii_chars = "⬛🟫🟧🟨⬜"
```

### 📐 Output Width Settings

| Width | Best For | Terminal Size |
|-------|----------|---------------|
| 40 | Low detail, fast | 40+ columns |
| 80 | Standard (Default) | 80+ columns |
| 120 | High detail | 120+ columns |
| 160 | Very high detail | 160+ columns |
| 200+ | Maximum detail | Wide displays |

### 🎞️ Frame Rate Settings

```python
fps = 0     # Auto-detect from video
fps = 15    # Low FPS (choppy but fast)
fps = 24    # Cinematic
fps = 30    # Smooth (Default)
fps = 60    # Very smooth (high CPU)
```

### 🔧 Advanced Configuration

```python
def play_video_in_terminal(
    video_path,
    width=80,           # Output width in characters
    fps=30,            # Frames per second
    frame_limit=None,  # Limit number of frames (None = all)
    clear_screen=True, # Clear terminal between frames
    ascii_chars=" .:-=+*#%@"  # Character set
):
    # Implementation
    pass
```

---

## 🎨 ASCII Character Set

### Understanding Character Density

ASCII characters have different visual densities:

```
Sparse ──────────────────────────────> Dense
  ' '    .    :    -    =    +    *    #    %    @
```

### Visual Representation

```
Character: ' '  .   :   -   =   +   *   #   %   @
Pixels:    ▁   ▂   ▃   ▄   ▅   ▆   ▇   █   ██  ███
Density:   0%  10% 20% 30% 40% 50% 60% 70% 80% 90%
```

### Character Set Comparison

```
Standard Set:     " .:-=+*#%@"
High Contrast:    " ░▒▓█"
Detailed:         " .'`^\":;Il!i<>~+_-?1|\\/tfjrxnuvczXY"
Simple:           " .oO@"
Blocks:           " ▁▂▃▄▅▆▇█"
```

---

## ⚡ Performance Tips

### 🚀 Optimization Strategies

#### **1. Reduce Output Width**
```python
# Faster rendering
play_video_in_terminal("video.mp4", width=40)
```

#### **2. Lower FPS**
```python
# Less CPU intensive
play_video_in_terminal("video.mp4", width=80, fps=15)
```

#### **3. Limit Frames**
```python
# Process only first N frames
frame_count = 0
while frame_count < 100:  # Limit to 100 frames
    # Process frame
    frame_count += 1
```

#### **4. Disable Screen Clearing**
```python
# Comment out clear command for faster output
# os.system('cls' if os.name == 'nt' else 'clear')
```

#### **5. Use Shorter Character Set**
```python
# Fewer characters = faster mapping
ascii_chars = " .oO@"
```

### 📊 Performance Metrics

| Setting | FPS | CPU Usage | Quality |
|---------|-----|-----------|---------|
| width=40, fps=15 | ~15 FPS | Low | Basic |
| width=80, fps=24 | ~24 FPS | Medium | Good |
| width=120, fps=30 | ~30 FPS | High | Excellent |
| width=160, fps=60 | ~40 FPS | Very High | Maximum |

---

## 🔧 Troubleshooting

<details>
<summary><strong>❌ Video file not found error</strong></summary>

**Error:**
```
Error: Video file 'video.mp4' not found.
```

**Solution:**
- Verify video file exists in project directory
- Check file name spelling (case-sensitive on Linux/Mac)
- Use absolute path: `/full/path/to/video.mp4`
- Supported formats: `.mp4`, `.avi`, `.mov`, `.mkv`
</details>

<details>
<summary><strong>❌ Import Error: No module named 'cv2'</strong></summary>

**Solution:**
```bash
pip install opencv-python
# OR
pip3 install opencv-python
```
</details>

<details>
<summary><strong>❌ Video plays too fast/slow</strong></summary>

**Solution:**
```python
# Adjust FPS manually
play_video_in_terminal("video.mp4", width=80, fps=24)

# Or let it auto-detect
play_video_in_terminal("video.mp4", width=80, fps=0)
```
</details>

<details>
<summary><strong>❌ ASCII output looks distorted</strong></summary>

**Causes:**
- Terminal window too small
- Incorrect aspect ratio

**Solutions:**
- Increase terminal size (maximize window)
- Reduce output width: `width=40`
- Use monospace font in terminal
- Adjust terminal line spacing
</details>

<details>
<summary><strong>❌ Performance issues / Lag</strong></summary>

**Solutions:**
```python
# Reduce width
play_video_in_terminal("video.mp4", width=40)

# Lower FPS
play_video_in_terminal("video.mp4", fps=15)

# Shorter character set
ascii_chars = " .oO@"
```
</details>

<details>
<summary><strong>❌ Terminal flickers</strong></summary>

**Solution:**
- Disable screen clearing for smoother output
- Comment out: `os.system('cls' if os.name == 'nt' else 'clear')`
- Trade-off: frames will overlap
</details>

---

## 🎭 Examples

### Example 1: Iron Man Video

```python
if __name__ == "__main__":
    video_path = "ironman.mp4"
    width = 100
    fps = 24
    
    play_video_in_terminal(video_path, width, fps)
```

### Example 2: Low-Res Quick Preview

```python
if __name__ == "__main__":
    video_path = "trailer.mp4"
    width = 40      # Low resolution
    fps = 15        # Lower FPS for speed
    
    play_video_in_terminal(video_path, width, fps)
```

### Example 3: High-Quality Output

```python
if __name__ == "__main__":
    video_path = "movie.mp4"
    width = 150     # High detail
    fps = 30        # Smooth playback
    
    play_video_in_terminal(video_path, width, fps)
```

### Example 4: Custom Character Set

```python
def play_custom_ascii(video_path):
    # Use block characters
    ascii_chars_custom = " ░▒▓█"
    
    # Modify convert function to use custom set
    # ... implementation
```

---

## 🎓 Advanced Usage

### 📹 Video Format Support

Supported formats via OpenCV:
- `.mp4` (MPEG-4)
- `.avi` (Audio Video Interleave)
- `.mov` (QuickTime)
- `.mkv` (Matroska)
- `.flv` (Flash Video)
- `.wmv` (Windows Media Video)

### 🎨 Color ASCII (Experimental)

Add ANSI color codes for colored ASCII:

```python
# ANSI color example
RED = '\033[91m'
GREEN = '\033[92m'
RESET = '\033[0m'

# Apply colors based on RGB values
colored_ascii = f"{RED}@{RESET}{GREEN}#{RESET}"
```

### 📊 Performance Monitoring

```python
import time

start_time = time.time()
frame_count = 0

# ... process frames

elapsed = time.time() - start_time
actual_fps = frame_count / elapsed
print(f"Actual FPS: {actual_fps:.2f}")
```

### 💾 Save ASCII Output to File

```python
def save_ascii_video(video_path, output_file, width=80):
    with open(output_file, 'w') as f:
        # Process frames
        f.write(ascii_art + "\n" + "="*width + "\n")
```

---

## 🤝 Contributing

Contributions welcome! Here's how:

### How to Contribute

1. **Fork** the repository
2. **Create** feature branch
   ```bash
   git checkout -b feature/ColorASCII
   ```
3. **Commit** changes
   ```bash
   git commit -m 'Add color ASCII support'
   ```
4. **Push** to branch
   ```bash
   git push origin feature/ColorASCII
   ```
5. **Open** Pull Request

### 💡 Contribution Ideas

- [ ] Add color ASCII support
- [ ] Implement audio playback
- [ ] Create GUI for parameter adjustment
- [ ] Add real-time webcam ASCII display
- [ ] Support for GIF export
- [ ] Add more character sets
- [ ] Improve performance optimization
- [ ] Create Docker container

---

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

---

## 📬 Contact

<div align="center">

### **Akshay Saitwal**

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=About.me&logoColor=white)](https://akshays-personal-portfolio.netlify.app/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akshay-saitwal-462bb4286/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/akshau094)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:akshaysaitwal9@gmail.com)


</div>

---

## 🙏 Acknowledgments

- **OpenCV Community** - Video processing capabilities
- **ASCII Art Community** - Inspiration and techniques
- **Python Community** - Amazing libraries and support

---

<div align="center">

### 💖 Show Your Support

⭐ Star this repo if you enjoyed terminal cinema!

![Wave](https://raw.githubusercontent.com/mayhemantt/mayhemantt/Update/svg/Bottom.svg)

**Made with 🐍 and ⌨️ by Akshay Saitwal**

<img src="https://komarev.com/ghpvc/?username=ascii-video-player&label=Project%20Views&color=00ff00&style=flat" alt="Profile views" />

</div>

---

<div align="center">

### 🎬 "Cinema was never meant to be this ASCII!"

**Happy Terminal Viewing! 🍿✨**

</div>
