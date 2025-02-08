# Technical Documentation Analysis Pipeline

## Project Goal
Development of a Large Language Model (LLM) specialized in technical documentation analysis and understanding.

## Current Phase: Building the Foundation
### 1. Named Entity Recognition (NER)
- Developing custom patterns to identify key technical entities
- Validating accuracy against manual counts
- Understanding entity occurrences and references

### 2. Relationship Extraction  
- Identifying connections between technical documents
- Capturing relationships between entities
- Building structured relationships for knowledge representation

### 3. Knowledge Graph Construction (Next Step)
- Converting extracted entities to nodes
- Using relationships as edges
- Creating a structured network of technical knowledge

## Implementation Progress
Currently focused on NER development:

### Entity Types Identified
- TECH_DOC (e.g., MCE0107B, TR 2043)
- SYSTEM_COMPONENT (e.g., MIDAS, NMCS2)
- HARDWARE_COMPONENT (e.g., Cabinet Type 600, AMI)
- COMMUNICATION_COMPONENT (e.g., RS485, Ethernet LAN)
- SUBSYSTEM_COMPONENT (e.g., Signal Subsystem)
- CONTROL_COMPONENT (e.g., Control System)
- SPECIFICATION_TYPE (e.g., Requirements Document)

### Current Features
- Custom spaCy NER patterns
- Case-insensitive matching
- Multiple format support
- Accuracy validation
- Performance visualization

## Requirements
- Python 3.x
- spaCy
- pdfplumber
- matplotlib
- prettytable
- numpy

## Project Roadmap
1. NER Development & Validation ← Current Stage
2. Relationship Extraction
3. Knowledge Graph Construction
4. LLM Development

## Usage
[To be added as components are completed]

## Contributing
[Guidelines to be added]

## License
[License information to be added]
