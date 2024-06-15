## 🚀 Features

- **🔍 Multimodal Analysis**: Leverages both visual and textual data for comprehensive image quality assessment.
- **🎨 Customizable Prompts**: Allows users to define personalized criteria for evaluating image aesthetics.
- **🤖 Advanced AI Model**: Utilizes CLIP (Contrastive Language-Image Pretraining) for precise and context-aware image evaluations.

## 📦 Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Image_Quality_Assessment.git
   cd Image_Quality_Assessment

2. **Install Dependencies:**:
   ```bash
   pip install torch torchvision pillow lavis pandas

## 🛠️ Usage

You can upload your images to the repository and use the provided functions to evaluate their aesthetic scores. Follow these steps:

1. **Step 1: Load and Process Images**: Place your images in the `images` folder.
2. **Step 2: Customize Prompts**: Modify the `cls_names` list to use your own descriptions for good(Postives) and bad(Negatives) photos.
3. **Step 3: Run the Evaluation Script**: Modify the `img_files` list in the evaluation script to include the paths to your uploaded images.

   ```python
   img_files = ['images/your_image1.jpg', 'images/your_image2.jpg']

## 🎨 Examples
Evaluating a Single Image
 ```python
  from PIL import Image
  
  img = Image.open("path/to/your/image.jpg")
  aesthetics_score = score_image(img)
  print(f"Aesthetics Score: {aesthetics_score}")
```

Batch Evaluation
 ```python
img_files = ["path/to/your/image1.jpg", "path/to/your/image2.jpg"]
scores = []
for img_file in img_files:
    img = Image.open(img_file)
    aesthetics_score = score_image(img)
    scores.append({'img': img_file.split('/')[-1], 'score': aesthetics_score})
    print(f"{img_file.split('/')[-1]} - Aesthetics Score: {aesthetics_score}")

import pandas as pd
pd.DataFrame(scores).describe()
```
## 🤝 Contributing
We welcome contributions to enhance this project! Feel free to submit issues or pull requests on GitHub.
