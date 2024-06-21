# ACSAC 2024 submission #101 Artifact
# Description

This is the dataset used to evaluate the ACSAC 2024 submission #101: *ScamFerret: Detecting Scam Websites Autonomously with Large Language Models*.


## Directory Tree

<pre>
.
├── README.md
├── dataset
│   ├── legitimate_websites
│   │   ├── cryptocurrency
│   │   │   ├── groundtruth_url.txt
│   │   │   └── toppage_html
│   │   ├── investment
│   │   │   ├── ...
│   │   ├── online_shopping_english
│   │   │   ├── ...
│   │   ├── online_shopping_german
│   │   │   ├── ...
│   │   ├── online_shopping_japanese
│   │   │   ├── ...
│   │   └── technical_support
│   │       ├── ...
│   └── scam_websites
│       ├── cryptocurrency
│       │   ├── groundtruth_url.txt
│       │   └── toppage_html
│       ├── investment
│       │   ├── ...
│       ├── online_shopping_english
│       │   ├── ...
│       ├── online_shopping_german
│       │   ├── ...
│       ├── online_shopping_japanese
│       │   ├── ...
│       └── technical_support
│           ├── ...
├── evaluation
│   ├── classification_accuracy.ipynb
│   ├── explainabilty.ipynb
│   ├── geminipro_results
│   │   ├── classification_accuracy
│   │   │   ├── legitimate_websites
│   │   │   │   ├── cryptocurrency
│   │   │   │   ├── investment
│   │   │   │   ├── online_shopping_english
│   │   │   │   ├── online_shopping_german
│   │   │   │   ├── online_shopping_japanese
│   │   │   │   └── technical_support
│   │   │   └── scam_websites
│   │   │       ├── cryptocurrency
│   │   │       ├── investment
│   │   │       ├── online_shopping_english
│   │   │       ├── online_shopping_german
│   │   │       ├── online_shopping_japanese
│   │   │       └── technical_support
│   │   └── explainability
│   │       ├── legitimate_websites
│   │       │   ├── cryptocurrency
│   │       │   ├── investment
│   │       │   ├── online_shopping_english
│   │       │   ├── online_shopping_german
│   │       │   ├── online_shopping_japanese
│   │       │   └── technical_support
│   │       └── scam_websites
│   │           ├── cryptocurrency
│   │           ├── investment
│   │           ├── online_shopping_english
│   │           ├── online_shopping_german
│   │           ├── online_shopping_japanese
│   │           └── technical_support
│   ├── gpt-3.5_results
│   │   ├── classification_accuracy
│   │   │   ├── legitimate_websites
│   │   │   │   ├── ...
│   │   │   └── scam_websites
│   │   │       ├── ...
│   │   └── explainability
│   │       ├── legitimate_websites
│   │       │   ├── ...
│   │       └── scam_websites
│   │           ├── ...
│   ├── gpt-4_results
│   │   ├── classification_accuracy
│   │   │   ├── legitimate_websites
│   │   │   │   ├── ...
│   │   │   └── scam_websites
│   │   │       ├── ...
│   │   └── explainability
│   │       ├── legitimate_websites
│   │       │   ├── ...
│   │       └── scam_websites
│   │           ├── ...
│   └── information_used.ipynb
└── prompt
    ├── evaluation_prompt.txt
    ├── prompt_template.txt
    └── single-turn_prompt.txt
</pre>


## Directory Descriptions

- **dataset/**: Ground-truth dataset evaluating the proposed system.
  - **legitimate_websites/**: Contains directories related to different types of legitimate websites.
    - **cryptocurrency/**:
      - `groundtruth_url.txt`: Contains ground-truth URLs.
      - `toppage_html/`: Directory for top page HTML files.
    - **investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `cryptocurrency/`, containing respective data and resources.
  - **scam_websites/**: Contains directories related to different types of scam websites.
    - **cryptocurrency/**,**investment/**, **online_shopping_english/**, **online_shopping_german/**, **online_shopping_japanese/**, **technical_support/**: Follow the same structure as `legitimate_websites/cryptocurrency/`, containing respective data and resources.

- **evaluation/**: Evaluation results of the proposed system using the ground-truth dataset.
  - **classification_accuracy/**: Results of the scam website classification accuracy evaluation in Section 5.2.
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
  - **explainablity/**: Evaluation results of the explainability of the basis for judging websites in Section 5.3.
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
  - `evaluation_prompt.txt`: Prompts used to evaluate the explainability of the website judgment basis.
  - `prompt_template.txt`: Prompt template used for analysis of scam websites in the proposed system.
  - `single-turn_prompt.txt`:Prompt used in the system for comparative evaluation.

- **README.md**: This readme file.
