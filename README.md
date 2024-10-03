# `SAAMANA-AUTO`

<p align="left">
	<img src="https://img.shields.io/github/last-commit/avi4h/saamana-auto?style=flat&logo=git&logoColor=white&color=green" alt="last-commit">
	<img src="https://img.shields.io/badge/Python-FFE01B?style=flat&logo=Python&logoColor=3776AB&color=white" alt="Python">
	<img src="https://img.shields.io/badge/GitHub%20Actions-2088FF.svg?style=flat&logo=GitHub-Actions&logoColor=white" alt="GitHub%20Actions">
    <img src="https://img.shields.io/badge/Ghostscript-purple.svg?style=flat&logo=gitee&logoColor=black" alt="GitHub%20Actions">
    <img src="https://img.shields.io/badge/Mailgun%20API-F06B66?style=flat&logo=mailgun&logoColor=white" alt="Mailgun%20API">
    <img src="https://img.shields.io/badge/Cron-DDF4FF?style=flat&logo=pythonanywhere&logoColor=black" alt="PythonAnywhere">
</p>
	
Efficient Python script that automates the daily download, merging, compressing, and email distribution of PDF file of Saamana e-newspaper. Concurrency techniques and secure HTTP requests, this script ensures timely and automated delivery of the newspaper to the specified recipient.

## 🚀 Setup

### 📦 Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/avi4h/saamana-auto.git
    cd saamana-auto
    ```

2. **Install dependencies**:
    ```sh
    python -m pip install --upgrade pip
    pip install requests PyPDF2
    ```

3. **Set up environment variables**:
    Create a `.env` file in the project directory with the following content:
    ```env
    MAILGUN_API_KEY=your-mailgun-api-key
    MAILGUN_DOMAIN=your-mailgun-domain
    RECEIVER_EMAIL=receiver-email@example.com
    ```

### 📄 PDF Compression

The script uses Ghostscript to compress the merged PDF file. Ensure Ghostscript is installed and added to your PATH.

- **Ghostscript Installation**:
  - **Windows**: Download and install from [Ghostscript Downloads](https://www.ghostscript.com/download/gsdnld.html).
  - **Linux**: Install via package manager, e.g., `sudo apt-get install ghostscript`.
  - **macOS**: Install via Homebrew, e.g., `brew install ghostscript`.

The compression settings used in the script are optimized for reducing file size while maintaining reasonable quality. 

### 🤖 GitHub Actions Configuration

1. **Add Secrets**:
    - Go to your GitHub repository.
    - Click on "Settings".
    - In the left sidebar, click on "Secrets and variables" and then "Actions".
    - Add the following secrets:
        - `MAILGUN_API_KEY`
        - `MAILGUN_DOMAIN`
        - `RECEIVER_EMAIL`

2. **Workflow Configuration**:
    The workflow is defined in `.github/workflows/schedule.yml` and is set to run daily at 2:30 AM UTC that is 8:00 AM IST. The workflow is written to run on Ubuntu. For other operating systems, you should make the necessary changes in `script.py` according to the operating system it is running on, as mentioned in the comments of the script.

## ⚙️ Support

If you encounter any issues with this repository or have any questions, please open an issue in the [Issues](https://github.com/avi4h/saamana-auto/issues) section. 

## 🚨 Legal 

If necessary, I can remove this repository upon request.

