# Roop Face Swap Deep Fake

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ranareehanaslam/Roop-Face-Swap-AI/blob/main/Roop_Face_Swap_Deep_Fake.ipynb)

Welcome to the Roop Face Swap Deep Fake project! This README will guide you through the process of using this notebook to create deep fake videos with face swapping. Whether you're a curious enthusiast or a developer looking to explore the world of deep learning and artificial intelligence, this project has something for everyone.

## About Roop Face Swap

Roop Face Swap is a project that enables you to perform face swapping on videos, creating deep fake content. With this tool, you can swap faces in videos, enhancing your creativity and having fun with AI-generated content.

## Demo Video

Before you get started, check out our [Demo Video](https://youtu.be/0RqWRB1vo_c) to see the exciting possibilities of Roop Face Swap in action.

## Project Links

- [Github Profile](https://github.com/ranareehanaslam): Visit our GitHub profile for updates and more AI projects.
- [Youtube Channel](https://www.youtube.com/@ranareehanaslam): Explore our YouTube channel for video tutorials and demonstrations.

## Getting Started

To create deep fake videos with Roop Face Swap, follow these steps:

### 1. Clone the Roop Repo and Install Dependencies

Open the notebook and run the following code to clone the Roop repository and install the required dependencies:

```python
!git clone https://github.com/s0md3v/roop.git
%cd roop
!pip install -r requirements.txt
```

### 2. Download the Model

Download the face swapping model by running the following code:

```python
!wget https://huggingface.co/ezioruan/inswapper_128.onnx/resolve/main/inswapper_128.onnx -O inswapper_128.onnx
!mkdir models
!mv inswapper_128.onnx ./models
```

### 3. GPU Support

If you have a GPU available, you can enhance the speed of deep fake generation. Run the following code to set up GPU support:

```python
!pip uninstall onnxruntime onnxruntime-gpu -y
!pip install torch torchvision torchaudio --force-reinstall --index-url https://download.pytorch.org/whl/cu118
!pip install onnxruntime-gpu
```

### 4. Create Deep Fake

Finally, use the following code to create a deep fake video:

```python
!python run.py --target '/content/bryan.mp4' --source '/content/tom.jpg' -o '/content/swapped.mp4' --execution-provider cuda --frame-processor face_swapper face_enhancer
```

Replace the file paths with your own source and target video/image.

## Enjoy Creating Deep Fakes!

Have fun creating deep fake videos with Roop Face Swap. Explore the possibilities, experiment with different faces, and share your creations with the world. Please use this technology responsibly and consider the ethical implications of deep fake content. Happy face swapping!

If you encounter any issues or have questions, feel free to reach out to us on our GitHub or YouTube channel. We're here to help!
