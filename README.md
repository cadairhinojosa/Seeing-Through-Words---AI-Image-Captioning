# Seeing Through Words App

## Project Overview
The "Seeing Through Words App" is an intelligent image analysis tool that processes uploaded images to provide a detailed text description, detect potential dangers (such as crime scenes or caution-worthy elements), and narrate the findings in audio format. It leverages state-of-the-art machine learning models for image captioning and object detection, making it useful for accessibility, safety monitoring, or general image understanding.

## Features
- **Image Captioning**: Generates a textual description of the uploaded image.
- **Danger Detection**: Identifies objects and scenarios that might indicate danger or caution (e.g., weapons, police, fire, specific vehicles, aggressive animals).
- **Crime Scene Flagging**: Specifically flags potential crime scenes based on a curated list of keywords and detected objects.
- **Audio Narration**: Converts the generated caption and safety status into an audio output for an accessible user experience.
- **User-Friendly Interface**: Utilizes Gradio for an easy-to-use web interface, allowing users to simply upload an image and receive instant analysis.

## Technologies Used
- **Python**: The core programming language.
- **Transformers Library**: For image captioning using the BLIP model (`BlipProcessor`, `BlipForConditionalGeneration`).
- **Ultralytics YOLOv8**: For efficient and accurate object detection (`YOLO`).
- **Gradio**: For creating the interactive web-based user interface.
- **gTTS (Google Text-to-Speech)**: For converting text analysis results into spoken audio.
- **PyTorch**: The underlying deep learning framework.

## How to Use
1.  **Install Dependencies**: Ensure all required Python packages are installed (as seen in the first code cell of this notebook: `transformers`, `torch`, `torchvision`, `ultralytics`, `gradio`, `gtts`).
2.  **Initialize Models**: The notebook will load the YOLOv8 model for object detection and the BLIP model for image captioning.
3.  **Define Danger Keywords**: A predefined list of keywords is used to identify potential dangers.
4.  **Run the Gradio Interface**: Execute the last code cell that initializes and launches the Gradio application.
5.  **Upload Image**: Once the Gradio interface is running (it will provide a local URL and a public URL), open it in your web browser.
6.  **Analyze**: Upload an image via the interface. The app will process it, display a caption and safety status, and provide an audio narration.

## Project Structure
- `!pip install ...`: Installation of necessary libraries.
- `import ...`: Importing Python modules.
- `model_yolo = YOLO(...)`: Loading the YOLO object detection model.
- `processor = BlipProcessor.from_pretrained(...)`: Loading the BLIP image captioning processor and model.
- `danger_keywords`: List of terms used for danger detection.
- `generate_caption(image)`: Function to generate a text caption for an image.
- `text_to_audio(text_input)`: Function to convert text into an audio file.
- `detect_danger(image)`: Function to detect dangerous objects or scenarios in an image.
- `analyze_image(img)`: The main function that orchestrates captioning, danger detection, and audio generation.
- `gr.Interface(...)`: Gradio interface setup for the web application.

## Potential Future Enhancements
- **Customizable Danger Keywords**: Allow users to define or modify danger keywords.
- **Real-time Video Analysis**: Extend functionality to analyze video streams in real-time.
- **More Sophisticated Danger Categories**: Introduce more granular categories for danger assessment (e.g., "environmental hazard," "personal threat").
- **Multi-language Support**: Provide captions and audio narration in multiple languages.
- **User Feedback Loop**: Implement a mechanism for users to provide feedback on analysis accuracy.
- **Deployment Options**: Explore deployment to cloud platforms for broader accessibility.
  
- # Demo Video
- 

![ImageCap1](https://github.com/user-attachments/assets/090fadab-9caf-413e-a4b1-f04573c013cf)
