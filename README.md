# Data Mining for CIBMTR Database Using AutoGen 

This project provides an implementation of AutoGen for data mining on the CIBMTR (Center for International Blood and Marrow Transplant Research) published database. 
The CIBMTR database contains comprehensive datasets related to hematopoietic cell transplantation (HCT) and cellular therapy for all published articles since 2019. 
Using a 6-party conversational agents, the primary outcomes of published articles can be replicated with a zero-shot prompt. 

## Introduction

AutoGen, developed by Microsoft in collaboration with Penn State University and the University of Washington, is an innovative multi-agent AI framework designed to manage and automate complex workflows involving large language models (LLMs). 
This project was build on the AutoGen platform with goal for autonomous data analysis and hypothesis generation from the data. 

![This is a demonstation of the 6-party agents](https://github.com/jwang-580/CIBMTR_data/blob/8495b4321bcd6ef64012ac34eb311ce0720341e0/data_files/6_party_agents.png)

## Features

- Data sets and corresponding data dictionary can be openly obtained from [CIBMTR data access](https://cibmtr.org/CIBMTR/Resources/Publicly-Available-Datasets)
- The data files (CSV) and corresponding data dictionaries (JSON) are automatically analysed with the 6-party agents
- Data dictionaries are retrieved with OAI agents to save token
- Various types of outcomes (e.g. baseline characteristics, survival analysis, Cox regression) can be replicated with a zero-shot prompt
- Outcome reporting and data visualization are optimized for scientific format
![This is a demonstration of zero-shot prompting](https://github.com/jwang-580/CIBMTR_data/blob/c30e5d6631cb3ab319159bbed7dc95ee18129d74/data_files/zero_shot_example.png)

## Getting Started

### Prerequisites

- OpenAI API key
- Python 3.x
- AutoGen version 0.2.0b5 or higher

### Required Python Libraries
```bash
pip install pandas numpy scikit-learn lifelines matplotlib autogen
```

### Agent Configuration

The system uses 6 specialized agents working together:

1. **Admin (UserProxyAgent)**: Executes code and manages human interaction
2. **Planner**: Creates data analysis plans and identifies required variables
3. **Data Retriever (GPTAssistantAgent)**: Accesses and retrieves data from data dictionaries
4. **Data Cleaner**: Validates and displays variables based on data dictionary
5. **Data Scientist**: Writes and adjusts Python code for analysis
6. **Reviewer**: Reviews analysis results and draws conclusions

### Environment Setup

Set your OpenAI API key in the environment:
```bash
export OPENAI_API_KEY=your_api_key
```


## Usage

The system can handle various analysis tasks including:
- Survival analysis
- Cox regression
- Cumulative incidence calculations
- Baseline characteristics comparison
- Multivariable analysis

Each analysis is initiated with a natural language prompt specifying the desired outcome and analysis type.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- CIBMTR for providing the publicly available datasets

## Contact

For questions and support, please open an issue in the GitHub repository.


