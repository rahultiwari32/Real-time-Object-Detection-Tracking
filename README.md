# Real-time Object Detection and Tracking with Azure & OpenCV

## Project Overview

This project demonstrates a robust computer vision pipeline for real-time object detection and tracking. It leverages **Azure Cognitive Services** for powerful, pre-trained object detection and **OpenCV** for efficient, real-time video processing and visualization.

The solution is designed for efficiency, calling the Azure API only at set intervals and using simple state management to track objects in between API calls.

## Features

-   **Object Detection:** Utilizes the Azure Computer Vision API to identify common objects in a video stream.
-   **Real-time Tracking:** Continuously processes video frames from a webcam.
-   **Hybrid Approach:** Combines the high accuracy of a cloud-based AI service with the low-latency performance of a local computer vision library.
-   **Clean Architecture:** The project is structured for easy understanding, maintenance, and deployment.

## Technologies Used

-   **Python:** The core programming language.
-   **Azure Cognitive Services (Computer Vision):** For performing cloud-based object detection.
-   **OpenCV:** For video stream capture and drawing annotations (bounding boxes, labels).

## Setup and Installation

### Prerequisites

-   A Microsoft Azure account.
-   An active **Computer Vision** resource on Azure. You will need its **Endpoint** and **API Key**.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    cd your-repo-name
    ```
2.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```

### Configuration

1.  Set your Azure credentials as environment variables or directly in the `main.py` file.
    -   `AZURE_VISION_ENDPOINT`
    -   `AZURE_VISION_KEY`

### How to Run the Project
Paste the Code: Copy the entire .ipynb script (provided below) and paste it into a code cell in your Google Colab notebook.

Update File Paths: In the if __name__ == "__main__": block, ensure the image_file and video_file paths correctly point to your files in Google Drive. For example:

Python

base_path = "/content/drive/My Drive/assets/" # Adjust if your assets folder is elsewhere
image_file = os.path.join(base_path, "sample_image.jpg")
video_file = os.path.join(base_path, "sample_video.mp4")
Choose Your Mode:

To process an image: Uncomment process_image(image_file) and ensure process_video(video_file) is commented out.

To process a video: Uncomment process_video(video_file) and ensure process_image(image_file) is commented out.

Run the Cell: Execute the code cell.

For video processing, a new window (within Colab's output) will display the video with detections. Press 'q' on your keyboard (while the video window is active) to stop processing.

For image processing, the detected image will be displayed.
