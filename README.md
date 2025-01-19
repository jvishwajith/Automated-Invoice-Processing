# OCR Field Extraction System 📄

## Project Objective 🎯
The OCR Field Extraction System addresses the challenge of automating document processing by extracting specific fields from images. Traditional manual data entry is time-consuming and error-prone, especially when dealing with large volumes of documents. This system automates the process using advanced computer vision and OCR technologies.

### Problem Statement
- Manual extraction of data from documents is inefficient
- High risk of human error in data entry
- Time-consuming process for large document volumes
- Inconsistent data formatting
- Need for structured data output

## Process and Approach 🔍

### Technologies Used
- **YOLO (You Only Look Once)** 🎯: For field detection and localization
- **Tesseract OCR** 📝: For text extraction
- **OpenCV** 👁️: For image processing
- **Python** 🐍: Core programming language
- **Pandas** 📊: For data structuring and export

### Key Features
1. **Automated Detection**: Uses YOLO to identify field locations
2. **Intelligent Text Extraction**: Employs Tesseract OCR with field-specific processing
3. **Structured Output**: Generates standardized CSV files
4. **Error Handling**: Robust error detection and logging
5. **GPU Acceleration**: Optional CUDA support for faster processing

## Pipeline Design 🔄

### 1. Pipeline Initialization 🚀
- **Configuration Loading**
  - Load YOLO model
  - Initialize logging system
  - Set up output directories
- **Input Validation**
  - Verify image formats
  - Check file accessibility
  - Validate model weights

### 2. Pipeline Processing Flow ⚙️

#### a. Image Processing Stage
```
Input Image → Preprocessing → YOLO Detection → Field Localization
```
- Loads document images
- Applies necessary preprocessing
- Detects field locations using YOLO
- Maps detected regions to field types

#### b. Text Extraction Stage
```
Field Regions → OCR Processing → Text Cleaning → Validation
```
- Extracts text from detected regions
- Applies field-specific processing rules
- Validates extracted content
- Handles multi-line text

#### c. Data Processing Stage
```
Raw Text → Field Processing → Data Structuring → Validation
```
- Processes extracted text based on field type
- Applies business rules and validations
- Structures data for output
- Handles special characters and formatting

### 3. Pipeline Output 📋
- **Data Export**
  - Generates CSV with extracted fields
  - Includes processing metadata
  - Maintains data structure
- **Logging and Reporting**
  - Records processing statistics
  - Documents any errors or warnings
  - Generates processing summary

### Supported Fields
| Field Type | Description | Processing Type |
|------------|-------------|-----------------|
| AWB-No | Airway Bill Number | Numeric |
| FOB-Value-in-INR | FOB Value in Indian Rupees | Currency |
| Goods-Description | Product Description | Text |
| Non-GST-Invoice-No | Invoice Number | Alphanumeric |
| Qty | Quantity | Numeric |
| Total-Value | Total Amount | Currency |
| Unit-Value | Per Unit Value | Currency |

## Getting Started 🚦

### Prerequisites
1. Python 3.8 or higher
2. CUDA-compatible GPU (optional)
3. Tesseract OCR installed

### Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/ocr-field-extraction.git

# Install dependencies
pip install -r requirements.txt

# Configure paths in config.py
# Place YOLO weights in models directory
```

### Usage
```python
# Run the pipeline
python src/main.py --input_dir /path/to/images --output_dir /path/to/output
```

## Results and Performance 📊
- **Accuracy**: High precision in field detection and extraction
- **Speed**: Processes multiple documents per second with GPU
- **Reliability**: Robust error handling and validation
- **Scalability**: Supports batch processing of large document volumes

## Future Enhancements 🔮
1. Web interface for document upload
2. API integration capabilities
3. Support for additional document types
4. Enhanced error recovery mechanisms
5. Cloud storage integration

## Contributing 🤝
Contributions are welcome! Please feel free to submit a Pull Request.

## License 📝
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support 💬
For support, please open an issue in the GitHub repository.

---

*Made with ❤️ by Vishwajith J*
