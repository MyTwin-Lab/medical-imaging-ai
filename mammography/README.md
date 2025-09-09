# Medical Mammography Imaging: Breast Cancer Screening

## Project Scope of Works

### Project Overview
This project involves building deep learning models to analyze screening mammograms for
signs of breast cancer. Targeted at intermediate to advanced-level data scientists, the
project will focus on leveraging state-of-the-art frameworks like MONAI to develop a robust
pipeline for breast density classification and lesion detection &amp; segmentation. The final
models will be integrated into a DICOM-standard workflow, demonstrating a path toward
clinical deployment.

### Why Breast Cancer Screening?
- **Massive and Systematic**: Screening programs generate a huge volume of images, creating
a significant need for AI-assisted tools.
- **Impactful**: Early diagnosis dramatically improves survival rates.
- **Well-Defined Use Case**: The clinical need is clear, and several AI tools are already CE/FDA
approved, providing a strong foundation.
- **AI Added Value**: AI can act as a second reader, reduce false negatives, and relieve the
workload for radiologists.
 Empowerment: A focus on women&#39;s health technology is a critical and impactful area for
innovation.

## Project Objectives

### Dataset Acquisition and Preprocessing:
- Utilize public mammography datasets (e.g., CBIS-DDSM, INbreast) for model training and
evaluation.
- Perform advanced preprocessing specific to mammography (e.g., breast segmentation,
intensity normalization) using MONAI Core transforms.

### Model Development:
- Build and train models for two key tasks:
  1. Breast Density Classification: A multi-class classification task.
  2. Lesion Detection &amp; Segmentation: Localizing and outlining suspicious masses or
calcifications.
- Leverage models from the MONAI Model Zoo (e.g., UNet, ResNet) as a starting point.
- Perform model evaluation, validation, and confidence calibration.
Clinical Integration &amp; Demo:
- Package the trained models into a DICOM-compliant application using MONAI Deploy.
- Generate DICOM Structured Reports (SR) to communicate findings in a standard clinical
format.
- Create a demo PACS viewer integration to show AI overlays and results.

## Technical Requirements

### Tools and Libraries:
- Medical Imaging Framework: MONAI Core, MONAI Label, MONAI Deploy
- Deep Learning Framework: PyTorch
- Medical Standard Handling: highdicom, pydicom
- Data Handling: NumPy, Pandas
- Visualization: matplotlib, Seaborn

### Environment:
- Python 3.8+
- NVIDIA GPU with CUDA support is highly recommended.
- Key Libraries: monai, torch, pydicom, highdicom, numpy, pandas, matplotlib, seaborn.

## Detailed Project Timeline

### Phase 1: Clinical Scoping &amp; Setup (Weeks 1-2)

#### Week 1 Activities:

**Clinical Use Case Definition**:
- Stakeholder meetings with radiologists
- Define intended use and clinical outputs
- Establish success metrics and evaluation criteria

**Regulatory Planning**:
- Data Protection Impact Assessment (DPIA) initiation
- Compliance framework establishment
- Ethical approval requirements review

#### Week 2 Activities:

**Dataset Preparation**:
- CBIS-DDSM dataset acquisition and organization
- INbreast dataset acquisition and organization
- Data licensing verification

**Annotation Protocol Development**:
- Standardized annotation guidelines creation
- Quality control procedures definition
- Inter-rater reliability assessment plan

### Phase 2: Rapid Annotation &amp; Pipeline Setup (Weeks 2-4)

#### Week 2-3 Activities:

**MONAI Label Setup**:
- Server installation and configuration
- Annotation interface customization
- Radiologist training sessions

**Initial Annotation Sprint**:
- Breast density annotation (200+ studies)
- Lesion bounding box annotation (100+ studies)
- Quality assurance on annotated data

#### Week 3-4 Activities:

**MONAI Core Pipeline**:
- Data preprocessing implementation (resizing, normalization)
- Custom transform development for mammography
- Data augmentation strategy implementation

**Model Selection**:
- MONAI Model Zoo evaluation
- Architecture selection (UNet vs. ResNet variants)
- Pre-trained model adaptation strategy

### Phase 3: Model Training & Validation (Weeks 3-6)

#### Week 3-4 Activities:

**Initial Model Training**:
- Breast density classification model training
- Hyperparameter optimization
- Cross-validation setup

**Validation Framework**:
- Data splitting (train/validation/test)
- Evaluation metrics implementation
- Baseline model establishment

#### Week 5 Activities:

**Lesion Detection Model**:
- Object detection model training
- Anchor box optimization for mammography
- Non-maximum suppression tuning

**Model Calibration**:
- Temperature scaling implementation
- Confidence calibration validation
- Uncertainty quantification

#### Week 6 Activities:

**Comprehensive Evaluation**:
- Seen data performance assessment
- Unseen data generalization testing
- Failure mode analysis

**Technical Reporting**:
- Initial performance metrics documentation
- Model limitations identification
- Next steps planning

### Phase 4: Advanced Tasks &amp; Multi-Center Evaluation (Weeks 6-8)

#### Week 6-7 Activities:

**Segmentation Task Addition**:
- Small annotated set creation (50+ studies)
- Segmentation model architecture selection
- Transfer learning from detection models

**Model Fine-tuning**:
- Joint detection-segmentation training
- Multi-task learning implementation
- Hyperparameter refinement

#### Week 7-8 Activities:

**Multi-Center Evaluation**:
- Public dataset testing (CBIS-DDSM, INbreast)
- Partner site data integration
- Cross-institution generalization assessment

**Performance Analysis**:
- Site-specific performance metrics
- Statistical significance testing
- Bias and variance analysis

### Phase 5: DICOM Integration & Demo (Weeks 8-10)

#### Week 8-9 Activities:

**MONAI Deploy Integration**:
- DICOM-SR output generation implementation
- Standardized reporting templates creation
- Clinical workflow integration design

**PACS/Viewer Demo Development**:
- AI overlay visualization implementation
- Interactive feedback mechanism
- Results display interface

#### Week 9-10 Activities:

**Radiologist Feedback Sessions**:
- Usability testing with clinical staff
- Workflow integration assessment
- Clinical relevance validation

**UX Refinement**:
- Interface improvements based on feedback
- Performance optimization
- Error handling enhancement

### Phase 6: Reader Study &amp; Final Packaging (Weeks 10-12)

#### Week 10-11 Activities:

**Reader Study Preparation**:
- Study protocol development
- Radiologist recruitment (10-15 participants)
- Case selection and randomization

**Study Execution**:
- Control vs. AI-assisted reading sessions
- Data collection (diagnoses, confidence levels, reading time)
- Blinded evaluation setup

#### Week 11-12 Activities:

**Gain Analysis**:
- Sensitivity/specificity comparison
- Reading time reduction quantification
- Diagnostic confidence improvement assessment

**Final Packaging**:
- Comprehensive technical report preparation
- Deployment package creation
- Documentation finalization

**Project Review**:
- Lessons learned session
- Future improvements identification
- Publication planning

### Key Milestones
1. Week 2: Clinical use case finalized and datasets acquired
2. Week 4: Initial annotation completed and pipeline operational
3. Week 6: Base models trained and validated
4. Week 8: Multi-center evaluation completed
5. Week 10: DICOM integration demonstrated
6. Week 12: Reader study concluded and final report delivered

### Risk Mitigation Strategies
- Data Quality: Regular annotation review sessions and quality checks
- Model Performance: Multiple architecture experiments and ensemble approaches
- Clinical Integration: Early and frequent engagement with radiologists
- Timeline: Buffer periods built into each phase for unexpected delays

## Getting Started
Follow these steps to set up the project locally:

1. Fork the Repository
To work on your own copy of this project:
1. Navigate to the MyTwin GitHub repository for this project.
2. Click the Fork button in the top-right corner of the repository page.
3. This will create a copy of the repository under your GitHub account.

2. Clone the Repository
After forking the repository:
1. Open a terminal on your local machine.
2. Clone your forked repository by running:
bash
git clone https://github.com/&lt;your-username&gt;/&lt;repository-name&gt;.git
3. Navigate to the project directory:
```bash
cd &lt;repository-name&gt;
```
3. Create a Virtual Environment
Setup a virtual environment to isolate project dependencies.
1. Run the following command in the terminal to create a virtual environment:
```bash
python3 -m venv .venv
```
2. Activate the virtual environment:
o On macOS/Linux:
```bash
source .venv/bin/activate
```
o On Windows (PowerShell):
```powershell
.venv\Scripts\Activate.ps1
```
o On Windows (Command Prompt):
```cmd
.venv\Scripts\activate.bat
```
3. Verify the virtual environment is active (the shell prompt should show (.venv)).
4. Install Dependencies
Install the required libraries for the project. It is recommended to install PyTorch first
following the official instructions for your CUDA version, then install MONAI and other
dependencies.
1. Example command for installing PyTorch (check the website for the correct command):
bash
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
2. Install the core project dependencies from requirements.txt:
bash
pip install -r requirements.txt
