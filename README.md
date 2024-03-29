# Point Tracking

This script implements point tracking in a video using the Lucas-Kanade method. It allows users to select points on the first frame of a video interactively and tracks them across subsequent frames.

## Features

- Interactive point selection: Users can select points on the first frame of the video by clicking with the mouse.
- Visualization: Tracked points are visualized on each frame of the video.
- Output options: The script can create an output video with tracked points and save the tracked points data to a JSON file.
- Command-line interface: Easy-to-use command-line interface with options to specify input and output files.

## Requirements

- Python 3.x
- OpenCV (cv2)
- NumPy

## Usage

1. Clone the repository
    ```
    git clone https://github.com/ippen/point-tracker.git
    ```

2. Install the required dependencies using pip:

    ```
    pip install opencv-python numpy
    ```

3. Run the script with the following command:

    ```
    python point_tracking.py <video_path> [options]
    ```

    Replace `<video_path>` with the path to your input video file.

## Command-line Options

- `-o, --output_video`: Path to the output tracked video file. If not provided, the default output file will be `<input_video_name>_tracked.mp4`.
- `-j, --json_file`: Path to the JSON file to save the tracked points data. If not provided, the default JSON file will be `<input_video_name>_tracked_points.json`.
- `-n, --no_video`: Flag to disable the creation of the output video. If set, the script will only save the tracked points data to the JSON file.

## Example

```
python point_tracking.py input_video.mp4 -o output_video.mp4 -j tracked_points.json
```

This command will track points in `input_video.mp4`, create an output video with tracked points named `output_video.mp4`, and save the tracked points data to `tracked_points.json`.