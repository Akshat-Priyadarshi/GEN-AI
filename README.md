# 📰 News Research Tool - GenAI Project

A powerful Streamlit-based application that leverages Generative AI and Large Language Models to analyze news articles and provide intelligent question-answering capabilities. This tool enables users to process multiple news URLs simultaneously and extract meaningful insights through natural language queries.

## 🚀 Features

- **Multi-URL Processing**: Analyze up to 3 news articles simultaneously
- **Intelligent Document Parsing**: Automatically extracts and processes content from web URLs
- **Vector-based Search**: Uses FAISS (Facebook AI Similarity Search) for efficient document retrieval
- **LLM-powered Q&A**: Leverages Hugging Face models for natural language understanding
- **Source Attribution**: Provides sources for all answers to ensure transparency
- **Persistent Storage**: Saves processed embeddings for faster subsequent queries
- **User-friendly Interface**: Clean Streamlit web interface for easy interaction

## 🛠️ Tech Stack

- **Frontend**: Streamlit
- **LLM Integration**: Hugging Face Transformers (GPT-2)
- **Document Processing**: LangChain
- **Vector Database**: FAISS
- **Embeddings**: Hugging Face Embeddings
- **Text Processing**: RecursiveCharacterTextSplitter
- **Data Persistence**: Pickle

## 📋 Prerequisites

- Python 3.7+
- Hugging Face API Token

## ⚙️ Installation
```bash
1. **Clone the repository**
git clone https://github.com/Akshat-Priyadarshi/GEN-AI.git
cd GEN-AI

2. **Install dependencies**
pip install -r requirements.txt

3. **Set up Hugging Face API Token**
   - Get your API token from [Hugging Face](https://huggingface.co/settings/tokens)
   - Replace `"your_hugging_face_api_token"` in `main.py` with your actual token
```
## 🚦 Usage
```bash
1. **Start the application**
streamlit run main.py

2. **Using the tool**:
   - Enter up to 3 news article URLs in the sidebar
   - Click "Process URLs" to analyze the content
   - Wait for the processing to complete (embedding creation)
   - Enter your question in the main interface
   - Get AI-powered answers with source attribution
```
## 📁 Project Structure
```css
GEN-AI/
├── main.py # Main Streamlit application
├── requirements.txt # Project dependencies
├── user_requests.csv # User interaction logs
├── faiss_store_huggingface.pkl # Cached vector embeddings (generated)
└── README.md # Project documentation
```
## 🔧 Configuration

### Model Parameters
- **Temperature**: 0.7 (controls response randomness)
- **Max Length**: 256 tokens
- **Max New Tokens**: 100
- **Chunk Size**: 500 characters for document splitting

### Supported Separators
The text splitter uses the following separators in order:
- `\n\n` (double newline)
- `\n` (single newline)
- `-` (hyphen)
- `,` (comma)

## 📊 Features in Detail

### **Document Processing Pipeline**
1. **URL Loading**: Extracts content from web articles
2. **Text Splitting**: Intelligently chunks documents for optimal processing
3. **Embedding Generation**: Creates vector representations using Hugging Face embeddings
4. **Vector Storage**: Stores embeddings in FAISS index for fast retrieval

### **Question Answering System**
- Uses RetrievalQAWithSourcesChain for context-aware responses
- Provides source attribution for transparency
- Maintains conversation context for follow-up questions

## 🔍 Example Use Cases

- **Financial News Analysis**: Process financial articles and ask about market trends
- **Research Assistance**: Analyze multiple research papers simultaneously
- **Content Summarization**: Extract key insights from lengthy articles
- **Fact Checking**: Cross-reference information across multiple sources

## 🐛 Known Issues & Fixes

1. **Line 42**: `urls=Urls` should be `urls=urls` (case sensitivity)
2. **Line 58**: Missing closing parenthesis in `chunk_size=500`
3. **Line 76**: `pickl.load(f)` should be `pickle.load(f)`
4. **Line 85**: `sources:` should be `sources` in the dictionary key

## 🚀 Future Enhancements

- [ ] Support for PDF document processing
- [ ] Integration with more advanced LLMs (GPT-4, Claude)
- [ ] Real-time news feed integration
- [ ] Export functionality for Q&A sessions
- [ ] Multi-language support
- [ ] Enhanced UI/UX with custom themes

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Akshat Priyadarshi**
- GitHub: [@Akshat-Priyadarshi](https://github.com/Akshat-Priyadarshi)
- Email: idhnap2005@gmail.com

## 🙏 Acknowledgments

- Hugging Face for providing the LLM infrastructure
- LangChain for the document processing framework
- Streamlit for the web interface framework
- Facebook AI for the FAISS vector search library

---

⭐ Don't forget to star this repository if you found it helpful!

