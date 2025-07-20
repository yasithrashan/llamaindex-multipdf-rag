# Multi-PDF RAG with LlamaIndex

A Retrieval-Augmented Generation system for querying multiple PDF documents using Google's Gemini API and LlamaIndex, optimized for Google Colab.

## Features

- Process multiple PDF documents simultaneously
- Vector embeddings with Gemini embedding-001 model
- LLM responses using Gemini 2.5 Flash
- Persistent storage for efficient reuse
- Interactive question-answering interface
- Optimized for Google Colab environment

## Quick Start

1. **Open in Google Colab:**
   - Upload `Multi_PDF_RAG_with_LlamaIndex.ipynb` to Google Colab

2. **Set up API Key:**
   - In Colab, go to the key icon (🔑) in the left sidebar
   - Add a new secret named `geminiapikey`
   - Paste your Google Gemini API key as the value

3. **Upload Your PDFs:**
   - Upload your PDF files to the Colab environment
   - Update the `pdf_directory` list with your file paths:
   ```python
   pdf_directory = ['/content/your-file-1.pdf', '/content/your-file-2.pdf']
   ```

4. **Run All Cells:**
   - Execute all cells in sequence
   - The system will create vector embeddings and be ready for queries

## Usage

Query your documents:
```python
response = query_pdfs("What are the main topics discussed in the documents?")
print(response)
```

## Configuration

- **Chunk Size:** 1024 tokens (adjustable)
- **Embedding Model:** `models/embedding-001`
- **LLM Model:** `models/gemini-2.5-flash`
- **Retrieval:** Top 3 similar chunks
- **Response Mode:** Compact

## File Structure

```
├── Multi_PDF_RAG_with_LlamaIndex.ipynb    # Main notebook
├── storage/                               # Vector index storage (auto-created)
└── README.md
```

## Requirements

- Google Colab account
- Google Gemini API key
- PDF documents to analyze

## Example Output

The system can answer complex questions about your documents:
- Summarize key findings across multiple PDFs
- Extract specific information
- Compare content between documents
- Provide source attribution

## Troubleshooting

- **API Key Issues:** Ensure your Gemini API key is correctly stored in Colab secrets
- **PDF Upload:** Make sure PDF paths in `pdf_directory` match uploaded file locations
- **Memory Issues:** For large PDFs, consider reducing `chunk_size`

## License

MIT