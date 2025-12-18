CortexAI

An AI-Powered Behavioral Intelligence Framework for Cyber Threat Analysis

1. Project Overview

CortexAI is a modular, AI-driven behavioral intelligence framework for advanced network traffic analysis.
Unlike traditional signature-based systems, CortexAI learns generalized behavioral patterns to distinguish malicious activity from benign traffic, enabling detection beyond known malware families.

The project is designed for cybersecurity research and analytical demonstration, emphasizing:

Modular system design

Behavioral generalization

Model explainability

Ethical handling of sensitive detection logic

2. Problem Statement

Modern cyber threats evolve rapidly, rendering signature-based detection increasingly ineffective.
Most existing datasets and ML models overfit to family-specific patterns, limiting their ability to detect unknown or zero-day threats.

CortexAI addresses this gap by:

Learning behavioral characteristics of network traffic rather than malware signatures

Enabling controlled experimentation through a modular research pipeline

Maintaining ethical abstraction of sensitive detection logic

3. Dataset Creation & Behavioral Learning

CortexAI is trained on a self-created, balanced dataset composed of multiple ransomware families and benign network traffic.
The primary objective is behavioral learning, not family identification.

To demonstrate analytical rigor and research methodology, the dataset creation process is documented in:

📄 docs/dataset_creation.pdf

This documentation covers:

Sourcing of raw PCAP files from the University of Navarra Ransomware Repository

Log conversion, feature engineering, and preprocessing strategies

Labeling logic and dataset balancing decisions

Ethical considerations to preserve generalization and prevent misuse

Significance

Behavioral learning enables detection of previously unseen ransomware families

The dataset supports robust discrimination between malicious and benign traffic across diverse sources

Future Work

Expansion with additional traffic scenarios

Refinement of behavioral feature representations

Improved generalization across evolving threat patterns

Dataset distribution visualizations emphasize behavioral diversity rather than dataset inflation, reflecting a research-driven analytical approach.

4. Modular Pipeline Overview

CortexAI consists of independently containerized modules, each functioning as a standalone research tool:

Module	Purpose
Zeek Sensor	Captures live traffic or processes PCAP files
Log-to-CSV Converter	Converts raw logs with controlled manual folder selection
Feature Engine	Performs feature extraction on categorized logs
Labeling Engine	Handles feature merging and labeling operations
Inference Engine	Applies trained models to generate behavioral verdicts

Note: Internal detection logic, feature thresholds, and model internals are intentionally abstracted for security and IP protection.

5. Architecture & Activity Diagrams

Architecture Diagram — Visualizes all Dockerized modules from raw traffic ingestion to inference output

Activity Diagram — Illustrates execution flow, manual analyst decisions, and research-oriented control points

Dataset Pipeline Flowchart — Shows PCAP → CSV → Feature Engineering → Labeling workflow

📁 Diagrams are available in the diagrams/ directory.

6. System Testing & Generalization Results

CortexAI was evaluated against both known and previously unseen ransomware families, as well as benign traffic.

Key Results

Unseen Ransomware Families

100% detection accuracy on ransomware families not included during training

No prior family labels provided

Demonstrates true behavioral generalization

Benign Traffic

100% accuracy on live traffic captured from the host system

90–95% accuracy on Stratosphere Labs normal traffic datasets

Significance

Confirms learning of generalized malicious behavior

Demonstrates robustness beyond training data

Validates research-oriented system design and analytical rigor

7. Security & Intellectual Property Notice

To preserve research integrity and prevent misuse, the following are intentionally not publicly disclosed:

Behavioral detection rules

Feature weighting strategies

Model internals and thresholds

This repository focuses on:

System architecture

Analytical workflow

Dataset methodology (abstracted)

Evaluation results

Detailed internals can be shared under NDA for academic or professional review.

8. Future Work & Research Potential

Expand datasets with diverse network environments

Introduce additional explainability metrics

Integrate inference with real-time monitoring (research mode)

Publish anonymized analytical findings for academic research
