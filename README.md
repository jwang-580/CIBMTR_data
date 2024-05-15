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
- Install [Python 3.x](https://www.python.org/downloads/).
- Install necessary Python libraries: `pandas`, `numpy`, `scikit-learn`, `lifelines`, `matplotlib`
- Install AutoGen version 0.2.0b5 or higher to allow OpenAI agents

### Installation

- under construction

