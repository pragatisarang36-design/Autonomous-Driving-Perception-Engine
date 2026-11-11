# Autonomous Driving Perception Engine

**Developer: Pragati Sarang**  
GitHub: [pragatisarang36-design](https://github.com/pragatisarang36-design)

A computer vision-based perception system designed to process video footage and identify, track, and monitor objects in a scene using YOLOv8, OpenCV, and Python.

## Features

- YOLOv8-based object detection with confidence-based box coloring and labels.
- Multi-object tracking with unique IDs assigned to detected objects.
- Object movement history shown as trajectory trails.
- Per-frame velocity estimation and directional movement arrows.
- Interactive mouse click to lock onto a detected object, with a reset control.
- Zoom inset visualization for the locked target.
- Real-time video processing and display while frames are processed.
- Processed video output generation.
- HUD-style visual interface with object count, tracking status, and source-video time.
- Frame progress indicators in the video and terminal progress bar. The source video's FPS is used for output timing.

## Technologies Used

- Python
- OpenCV
- NumPy
- YOLOv8 (Ultralytics)
- PyTorch (installed as a dependency of Ultralytics)
- tqdm

## Project Structure

```text
cv_projects-main/
├── Autonomous Driving Perception.py
├── LICENSE
└── README.md
```

The script loads the `yolov8n.pt` model through Ultralytics. The application automatically installs its listed Python dependencies (`opencv-python`, `numpy`, `ultralytics`, and `tqdm`) when they are missing. Ultralytics handles the PyTorch dependency.

## Installation and Execution

Open PowerShell or Command Prompt and clone the repository:

```powershell
git clone <repository-url>
cd cv_projects-main
```

Run the application with a video file as the first argument and an output video filename as the optional second argument:

```powershell
python "Autonomous Driving Perception.py" "path\to\input-video.mp4" "processed-output.mp4"
```

For example, if the input video is in the repository folder:

```powershell
python "Autonomous Driving Perception.py" "drive.mp4" "drive-processed.mp4"
```

If you omit the output filename, the processed video is saved as `yolovx_output.mp4` in the current working directory. The script opens a window for live viewing and writes the annotated frames to the output file.

## Controls

| Key / Action | Function |
| --- | --- |
| `Q` | Quit processing |
| `R` | Reset target lock |
| `SPACE` | Pause / Resume |
| Mouse click | Select and lock a detected object for tracking |

## Disclaimer

This project is intended for research and educational purposes. It is a computer vision research project that demonstrates object detection and tracking on video footage. It does not independently control autonomous vehicles and does not guarantee road safety. Do not rely on its output for vehicle operation or safety-critical decisions.
