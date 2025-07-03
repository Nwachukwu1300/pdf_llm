# Technical Document Knowledge Graph Project

## Overview

This project implements a knowledge graph system for technical documentation analysis and relationship extraction. It processes PDF documents, extracts named entities, and builds a graph structure to understand relationships between technical documents.

## 🎯 Project Goals

- **Knowledge Transfer**: Capture institutional knowledge from technical documentation
- **Faster Information Retrieval**: Enable rapid access to interconnected technical information
- **Relationship Discovery**: Automatically identify how technical documents reference each other
- **Engineering Support**: Provide an AI-powered assistant for technical document queries

## 📋 Features

- **PDF Text Extraction**: Extract and clean text from technical PDF documents
- **Named Entity Recognition**: Identify technical document codes and references
- **Relationship Extraction**: Determine how documents relate to each other
- **Knowledge Graph Construction**: Build graph representations of document relationships
- **Interactive Visualization**: Create visual representations of document networks
- **Chunking and Processing**: Handle large documents through intelligent text segmentation

## 🏗️ Architecture

### Core Components

1. **Text Processing Pipeline**
   - PDF text extraction using `pdfplumber`
   - Text cleaning and normalization
   - Chunking for manageable processing

2. **NLP Pipeline**
   - Custom spaCy pipeline with technical document patterns
   - Named Entity Recognition for document codes
   - Relationship type classification

3. **Knowledge Graph**
   - Entity extraction and normalization
   - Relationship discovery and classification
   - RDF triple generation
   - Graph analysis and statistics

4. **Visualization**
   - Network graphs using NetworkX and Matplotlib
   - Interactive relationship exploration
   - Statistical analysis dashboards

## 🔧 Technical Stack

- **Python 3.8+**
- **spaCy**: NLP processing and entity recognition
- **NetworkX**: Graph construction and analysis
- **pdfplumber**: PDF text extraction
- **Pandas**: Data manipulation and analysis
- **Matplotlib/Seaborn**: Visualization
- **Jupyter Notebooks**: Interactive development



### Basic Usage

1. **Prepare your documents**: Place PDF files in the `data/sample_documents/` directory

2. **Run the main notebook**: Open `PDF LLM MAIN V4.ipynb` in Jupyter

3. **Follow the pipeline**:
   - Text extraction from PDFs
   - Entity recognition and relationship extraction
   - Knowledge graph construction
   - Visualization and analysis

## 📊 Key Functionalities

### 1. Document Processing
- Extracts text from PDF documents
- Cleans and normalizes text content
- Removes irrelevant sections (headers, footers, references)
- Chunks large documents for processing

### 2. Entity Recognition
- Identifies technical document codes (e.g., DOC001, SPEC123)
- Recognizes various document formats and patterns
- Normalizes entity names for consistency

### 3. Relationship Extraction
- Determines relationship types between documents:
  - `references`: One document cites another
  - `supersedes`: One document replaces another
  - `relates_to`: General relationship between documents
- Extracts context around relationships

### 4. Knowledge Graph Analysis
- Builds comprehensive document relationship networks
- Calculates graph metrics (centrality, clustering, etc.)
- Identifies key documents and connection patterns
- Generates insights about document interconnectedness

## 🔍 Example Use Cases

### 1. Document Discovery
Find all documents related to a specific technical topic:
```python
# Find all documents related to "communication protocols"
related_docs = find_related_documents("communication protocols")
```

### 2. Dependency Analysis
Understand document dependencies:
```python
# Get all documents that reference DOC001
dependencies = get_document_dependencies("DOC001")
```

### 3. Knowledge Gap Identification
Identify isolated or poorly connected documents:
```python
# Find documents with few connections
isolated_docs = find_isolated_documents(min_connections=2)
```

## 📈 Performance Metrics

The system provides various metrics to evaluate knowledge graph quality:

- **Coverage**: Percentage of documents with identified relationships
- **Accuracy**: Quality of extracted relationships (requires manual validation)
- **Connectivity**: Graph connectivity measures
- **Processing Speed**: Documents processed per minute

## 🎛️ Configuration

### Document Patterns
Customize document code recognition patterns in the NLP pipeline:
```python
# Add new document patterns
doc_patterns = [
    {"LOWER": {"REGEX": r"^doc\d{4}[a-z]?$"}},  # DOC0001, DOC0001A
    {"LOWER": {"REGEX": r"^spec\d{3}[a-z]?$"}}, # SPEC001, SPEC001B
]
```

### Relationship Types
Configure relationship extraction rules:
```python
relationship_types = {
    "references": ["references", "refers to", "see also"],
    "supersedes": ["replaces", "supersedes", "obsoletes"],
    "relates_to": ["related to", "associated with"]
}
```


## ⚠️ Known Limitations

- **PDF Quality**: Performance depends on PDF text extraction quality
- **Domain Specific**: Optimized for technical documentation patterns
- **Manual Validation**: Relationship accuracy requires domain expert review
- **Scalability**: Large document sets may require distributed processing

# Contributions: 
Mmesoma Nwachukwu. 2025 - Sole Developer, Researcher  
