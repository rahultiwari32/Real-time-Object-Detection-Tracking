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

### How to Run

1.  From your terminal, run the main script:
    ```bash
    python main.py
    ```
2.  Press the 'q' key to exit the application.
