## 🔍 Overview

This project implements a real-time traffic light detection system within the CARLA simulator using YOLOv5. The system identifies traffic lights, classifies their color (red/green), calculates the distance from the ego vehicle to the nearest traffic light, and displays a contextual HUD message (`STOP!` or `DRIVE NOW!`) with the measured distance.

## 🛠️ Development Steps

1. **🖥️ CARLA Setup and Connection**: Install the CARLA simulator (Town01) and initialize a connection using `carla.Client`.  
2. **📦 Dependencies Installation**: Install required Python libraries: OpenCV, PyTorch, YOLOv5 (and related dependencies), and CARLA Python API.  
3. **🚀 Model Loading**: Load the pre-trained YOLOv5s model via `torch.hub.load` for real-time object detection.  
4. **🎥 Frame Streaming**: Use `camera.listen()` to stream camera frames from the simulator and convert each frame into a NumPy array for processing.  
5. **🔦 Detection, Classification, and HUD Display**: Detect traffic light bounding boxes with YOLOv5, classify the light color using HSV filtering, compute the Euclidean distance to the nearest traffic light, and overlay a HUD message in the bottom-left corner showing the action (`STOP!` or `DRIVE NOW!`) along with the distance.

6. 📂 Developed for the Software development for an intelligent autonomous vehicle course at Holon Institute of Technology (HIT)
