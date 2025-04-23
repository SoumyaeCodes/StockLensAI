To run the final chatbot, check out the App folder.
## *Required API Keys*  
Before running the project, ensure you have the following API keys set up in your environment variables:  

⁠ bash
export TAVILY_API_KEY="your_tavily_api_key"
export AWS_ACCESS_KEY_ID="your_aws_access_key"
export AWS_SECRET_ACCESS_KEY="your_aws_secret_access_key"
export AWS_DEFAULT_REGION="your_aws_region"
 ⁠

## Setting Up Your Development Environment
For an efficient development experience, please follow these two essential steps:
### 1. Install the Virtual Environment
First, create an isolated environment to house your project dependencies. Execute the following commands:

⁠ bash
# For Windows
python -m venv venv
# For macOS and Linux
python3 -m venv venv
 ⁠

### 2. Install All Required Libraries
Next, activate your virtual environment and install the necessary libraries in one swift command:

⁠ bash
# For Windows
.\venv\Scripts\activate
# For macOS and Linux
source venv/bin/activate
# Install all dependencies
pip install -r requirements.txt
 ⁠
