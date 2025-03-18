# 🖼️ Text-to-Image Generation using Stable Diffusion
This project generates high-quality images from user-provided text prompts using **Stable Diffusion**. It leverages the **diffusers library** and **StableDiffusionPipeline** from ***Hugging Face*** to create customized images based on user imagination.

---

## 📚 Table of Contents  

- ✨ **[Features](#-features)**  
- 🛠️ **[Installation and Setup](#-installation-and-setup)**  
- 🚀 **[How to Run the Script](#-how-to-run-the-script)**  
- 📂 **[File Structure](#-file-structure)**  
- 💡 **[Key Functions Explained](#-key-functions-explained)**  
- 🖼️ **[Screenshots (Example Outputs)](#-screenshots-example-outputs)**  
- 🌟 **[Dependencies](#-dependencies)**  
- 📋 **[How to Use](#-how-to-use)**  
- 📧 **[Contact](#-contact)**  

---

## ✨ Features

- **Text-to-Image Generation**  
  Generates high-quality images from natural language prompts using Stable Diffusion.

- **Stable Diffusion v1.5**  
  Utilizes the powerful and open-source **Stable Diffusion v1.5** model from Hugging Face for image generation.

- **Custom Prompts**  
  Users can input their own creative text prompts to generate unique images.

- **Negative Prompts**  
  Helps avoid unwanted elements or features in the generated images by specifying negative prompts.

- **Customizable Parameters**  
  Fine-tune the generation process with adjustable parameters:  
  - `Guidance Scale`: Controls how closely the output matches the prompt.  
  - `Inference Steps`: Defines the number of steps for higher-quality images.  
  - `Image Size`: Set custom height and width for output images.

- **Image Display**  
  Outputs and displays the generated image directly within the notebook using **Matplotlib**.

  ---

## 🛠️ Installation and Setup

Follow these steps to set up and run the project locally:

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/text-to-image-stable-diffusion.git
cd text-to-image-stable-diffusion
```

### 2. Install Python
Ensure Python (version 3.8 or higher) is installed. Download it from [python.org](https://www.python.org/).

### 3. Install Required Libraries and Dependencies

Run the following commands to install all the necessary libraries:
```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
pip install diffusers==0.25.0 transformers accelerate matplotlib

```
---

## 🚀 How to Run the Script

We can run the Text-to-Image Generation script either **locally** or on **Google Colab**.

### ▶️ Run on Google Colab

1. Open the Colab Notebook: [Google Colab Link](https://colab.research.google.com/)
2. Install dependencies inside Colab:

```bash
   !pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
   !pip install diffusers==0.25.0 transformers accelerate matplotlib
   
```

### ▶️ Run Locally

Follow these steps to run the project on your local machine:

### 1. Clone the Repository
git clone https://github.com/your-username/text-to-image-stable-diffusion.git
cd text-to-image-stable-diffusion

### 2. Install Required Libraries and Dependencies

Run the following commands to install all the necessary libraries:
```bash
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
pip install diffusers==0.25.0 transformers accelerate matplotlib
```

### 3. Run the Script
python generate.py

---

## 📂 File Structure
```
text-to-image/
│
├── Text_To_Image.ipynb  # Google colab
├── generated_images/    # Folder to save output images
└── README.md            # Project Documentation
```

---

## 💡 Key Functions Explained

### `load_model()`
- Loads the **Stable Diffusion v1.5** model from Hugging Face Hub.
- Uses `torch.float16` for optimized GPU performance.
- Moves the model to **GPU** if available; otherwise runs on **CPU**.

---

### `get_user_prompt()`
- Takes a **text prompt** from the user for image generation.
- Defines a **negative prompt** to avoid unwanted features in the output image.

---

### `set_generation_parameters()`
- Configures key parameters for image generation:
  - `guidance_scale`: Controls prompt adherence (recommended 7–9).
  - `num_inference_steps`: Sets diffusion steps for image quality (commonly 50–80).
  - `height` and `width`: Specifies output image resolution (default 512x512).

---

### `generate_image(user_prompt, negative_prompt, guidance_scale, num_inference_steps, height, width)`
- Runs the **Stable Diffusion pipeline** with the specified prompts and parameters.
- Returns the generated image as output.

---

### `display_image(generated_image)`
- Displays the generated image using **Matplotlib**.
- Hides axes for a cleaner view.

---
## 🖼️ Screenshots (Example Output)
1. **A futuristic city skyline at night**
![A futuristic city skyline at night]![1st_IMage](https://github.com/user-attachments/assets/07a5af7d-6e81-44cf-9713-9f9f254ad48f)

2. **Astronaut riding a lion on Mars, concept art**
![2nd_Image](https://github.com/user-attachments/assets/b571ab51-23cf-4fb4-89da-d2cb8249b667)

3. **A aeroplane fly obove the water**   
![3rd_image](https://github.com/user-attachments/assets/02ab4b4a-e1ff-4732-9369-f26937cfb4db)

4. **school kids walking with backpacks in a rural village, green fields and  traditional houses**  
![4th_image](https://github.com/user-attachments/assets/082e9282-32b0-45fa-9605-ac6da22d9a6d)

---

## 🌟 Dependencies List
-**Python >= 3.8** — To run the project
-**torch** — For deep learning and model processing
-**diffusers==0.25.0** — To use Stable Diffusion models
-**transformers** — Helps load and manage models
-**accelerate** — Makes the model run faster
-**matplotlib** — To display the generated images

---

## 📋 How to Use
1.-**Prompt Entry**: Run the script and enter your custom text prompt.
2.-**Image Generation**: The model will generate an image based on your input.
3.-**Visualization**: The image will be displayed using matplotlib.
4.-**Optional Saving**: Modify the script to save images to generated_images/ directory.

---

### 📧 Contact

- Email: ranjeetkumar4261770@gmail.com
- GitHub: [ranjeet5555](https://github.com/ranjeet5555)



