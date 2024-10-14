# Background Remover App

This app uses AI to quickly and effectively remove the background from images. Built using Flask and containerized with Docker, it's deployed via Google Cloud Run and utilizes the `rembg` AI model for background removal. The app is designed for easy use and provides seamless integration with cloud technologies for scalability.

## Features

- **Fast and accurate** background removal using the `rembg` AI model.
- **Containerized** with Docker for easy deployment and portability.
- **Hosted** on Google Cloud Run for scalability and reliability.
- **Image storage** handled by Google Cloud Storage.
  
## Tech Stack

- **Backend:** Flask
- **Containerization:** Docker
- **Hosting:** Google Cloud Run
- **AI Model:** `rembg`
- **Artifact Management:** Google Artifact Registry

## How It Works

1. Upload an image.
2. The app processes the image, removing the background.
3. Download the image with a transparent background.

## Prerequisites

- Docker installed on your system.
- Google Cloud CLI configured with appropriate permissions.

## Run Locally

1. Clone the repository:
    ```bash
    git clone https://github.com/samuelbauta/bg-remover.git
    ```
   
2. Navigate to the project directory:
    ```bash
    cd bg-remover-app
    ```

3. Build the Docker image:
    ```bash
    docker build -t bg-remover:latest .
    ```

4. Run the Docker container:
    ```bash
    docker run -p 5000:5000 bg-remover:latest
    ```

5. Access the app on `http://localhost:5000`.

## Demo

### User Interface
![UI Demo](https://github.com/user-attachments/assets/44abacab-b8be-4890-95bf-c47d87b1f67a)

### Before & After Background Removal
#### Original Image:
![Before Image](https://github.com/user-attachments/assets/b32b8503-74cb-4112-a640-68a7e540005b)

#### Background Removed:
![After Image](https://github.com/user-attachments/assets/d6703ec6-b554-4831-bd1d-6fe824de35af)

## Deployment

To deploy your own version, follow these steps:
1. Build and tag your Docker image.
2. Push the image to Google Artifact Registry.
3. Deploy to Google Cloud Run.

## License

This project is licensed under the MIT License.
