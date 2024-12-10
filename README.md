# DIMVA 2025 submission #60 Artifact
# Description

This is the implementation code, dataset, and evaluation results for the proposed system in the submission to DIMVA 2025 #60: *ScamFerret: Detecting Scam Websites Autonomously with Large Language Models*.

## Directory Tree

<pre>
.
├── README.md
├── dataset
│   ├── legitimate_websites
│   │   ├── cryptocurrency
│   │   │   ├── sample_screenshot
│   │   │   │   └── ...
│   │   │   ├── toppage_html
│   │   │   │   └── ...
│   │   │   └── groundtruth_url.txt
│   │   ├── investment
│   │   │   └── ...
│   │   ├── online_shopping_english
│   │   │   └── ...
│   │   ├── online_shopping_german
│   │   │   └── ...
│   │   ├── online_shopping_japanese
│   │   │   └── ...
│   │   └── technical_support
│   │       └── ...
│   └── scam_websites
│       ├── cryptocurrency
│       │   ├── sample_screenshot
│       │   │   └── ...
│       │   ├── toppage_html
│       │   │   └── ...
│       │   └── groundtruth_url.txt
│       ├── investment
│       │   └── ...
│       ├── online_shopping_english
│       │   └── ...
│       ├── online_shopping_german
│       │   └── ...
│       ├── online_shopping_japanese
│       │   └── ...
│       └── technical_support
│           └── ...
├── evaluation
│   ├── classification_accuracy.ipynb
│   ├── geminipro_results
│   │   ├── legitimate_websites
│   │   │   ├── cryptocurrency
│   │   │   ├── investment
│   │   │   ├── online_shopping_english
│   │   │   ├── online_shopping_german
│   │   │   ├── online_shopping_japanese
│   │   │   └── technical_support
│   │   └── scam_websites
│   │       ├── cryptocurrency
│   │       ├── investment
│   │       ├── online_shopping_english
│   │       ├── online_shopping_german
│   │       ├── online_shopping_japanese
│   │       └── technical_support
│   ├── gpt-3.5_results
│   │   ├── legitimate_websites
│   │   │   └── ...
│   │   └── scam_websites
│   │       └── ...
│   ├── gpt-4_results
│   │   ├── legitimate_websites
│   │   │   └── ...
│   │   └── scam_websites
│   │       └── ...
│   └── information_used.ipynb
└── prompt
│   ├── prompt_template.txt
│   └── single-turn_prompt.txt
└── system
    ├── content
    │   └──...
    ├── logs
    │   └── ...
    ├── results
    │   └──...
    ├── screenshot
    │   └── ...
    ├── .env
    ├── app.py
    ├── docker-compose.yml
    ├── Dockerfile
    ├── requirements.txt
    └── sample_urls.txt

</pre>


## Directory Descriptions

- **dataset/**: Ground-truth dataset evaluating the proposed system.
  - **legitimate_websites/**: Contains directories related to different types of legitimate websites.
    - **cryptocurrency/**:
      - `sample_screenshot/`: 20 screenshots for each type of scam and language (limited due to file size).
      - `toppage_html/`: Directory for top page HTML files.
      - `groundtruth_url.txt`: Contains ground-truth URLs.
    - **investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `cryptocurrency/`, containing respective data and resources.
  - **scam_websites/**: Contains directories related to different types of scam websites.
    - **cryptocurrency/**,**investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `legitimate_websites/cryptocurrency/`, containing respective data and resources.

- **evaluation/**: Evaluation results of the proposed system using the ground-truth dataset.
  - **geminipro_results/**: Experimental results with Gemini Pro for LLM.
    - **legitimate_websites/**: Contains directories related to different types of legitimate websites.
      - **cryptocurrency/**:
        - `[DomainName].json`: Each JSON file contains the analysis results for the specified domain name.
      - **investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `cryptocurrency/`, containing respective data.
    - **scam_websites/**: Contains directories related to different types of scam websites.
      - **cryptocurrency/**,**investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `legitimate_websites/cryptocurrency/`, containing respective data.
  - **gpt-3.5_results/**: Experimental results with GPT-3.5 for LLM.
    - **legitimate_websites/**: Contains directories related to different types of legitimate websites.
      - **cryptocurrency/**,**investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `geminipro_results/legitimate_websites/cryptocurrency/`, containing respective data.
    - **scam_websites/**: Contains directories related to different types of scam websites.
      - **cryptocurrency/**,**investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `geminipro_results/legitimate_websites/cryptocurrency/`, containing respective data.
  - **gpt-4_results/**: Experimental results with GPT-4 for LLM.
    - **legitimate_websites/**: Contains directories related to different types of legitimate websites.
      - **cryptocurrency/**,**investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `geminipro_results/legitimate_websites/cryptocurrency/`, containing respective data.
    - **scam_websites/**: Contains directories related to different types of scam websites.
      - **cryptocurrency/**,**investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `geminipro_results/legitimate_websites/cryptocurrency/`, containing respective data.

- **prompt/**: List of full prompts used in the paper.
  - `prompt_template.txt`: Prompt template used for analysis of scam websites in the proposed system.
  - `single-turn_prompt.txt`:Prompt used in the system for comparative evaluation.

- **system/**: Source code for the proposed system in the paper.
  - **content/**: The html content that the suggestion system saves when analyzing scam websites.
  - **logs/**: The logs from the execution of the proposal system.
  - **results/**: The results output by the proposal system
  - **screenshots/**: The screenshots that the proposal system saves when analyzing scam websites.
  - `.env`: This .env file needs to be set with API keys, etc.
  - `app.py`: Code that includes the processing that is the core of the system.
  - `docker-compose.yml`: Docker compose configuration file.
  - `Dockerfile`: Docker configuration file.
  - `requirements.txt`: File specifying python's dependent libraries.
  - `sample_urls.txt`: List of sample URLs for use in the proposal system input.

- **README.md**: This readme file.


## Project Setup and Execution

This project is an implementation of the proposed system based on Azure OpenAI Service and LangChain.

### 1. Navigate to the system directory
Before starting the setup process, navigate to the system directory in your terminal:

```
cd /path/to/system
```

Replace `/path/to/system` with the actual path to your project's system directory.

### 2. Create a .env file

Create a .env file in the project's root directory with the following content:

```
LOG_DIR="/app/logs/"
SAVE_CONTENT_DIR="/app/content"
SAVE_SCREENSHOT_DIR="/app/screenshots"
SAVE_LLM_RESPONSE_DIR="/app/results"
GOOGLE_API_KEY="xxxxxxxxxxxxxxx"
OPENAI_API_KEY="xxxxxxxxxxxxxxx"
OPENAI_API_TYPE="azure"
OPENAI_API_VERSION="2023-12-01-preview"
OPENAI_API_BASE="https://xxxxxxxxxxxxxxx.openai.azure.com/"
TAVILY_API_KEY="xxxxxxxxxxxxxxx"
LANGCHAIN_TRACING_V2="true"
LANGCHAIN_ENDPOINT="https://api.smith.langchain.com"
LANGCHAIN_API_KEY="xxxxxxxxxxxxxxx"
TWITTER_BEARER_TOKEN="xxxxxxxxxxxxxxx"
REDDIT_CLIENT_ID="xxxxxxxxxxxxxxx"
REDDIT_CLIENT_SECRET="xxxxxxxxxxxxxxx"
TARGET_URL_FILE="./sample_urls.txt"
ANALYSIS_LLM_TYPE="gpt-4"
```

Note: These API keys are sensitive information. Replace them with your own API keys when using in production.

### 3. Build the Docker image

Navigate to the project's root directory in your terminal and run the following command to build the Docker image:

```
docker compose build
```

### 4. Start the application

After the build is complete, start the application with the following command:

```
docker compose up -d
```

The `-d`option runs the container in detached mode, starting it in the background.

### 5. Stop the application

To stop the application, run:

```
docker compose down
```

This command stops and removes the containers created by docker compose up.
By following these steps, you can easily start and stop the application using Docker.