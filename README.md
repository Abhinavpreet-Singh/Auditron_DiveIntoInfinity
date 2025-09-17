# GenAI-Lawgic

A FastAPI-powered legal document simplifier and chatbot. Upload legal PDFs,
process them, and ask questions for instant, plain-language answers.

## Features

- Upload and process legal PDF documents
- Ask questions and get simplified answers
- Modern React frontend with responsive design
- Advanced clause analysis and risk assessment
- Real-time document processing progress

## Architecture

- **Backend**: FastAPI server (Python) - handles PDF processing, AI analysis,
  and API endpoints
- **Frontend**: React application - modern UI for document upload, viewing, and
  chat interface
- **Database**: FAISS vector store for document embeddings
- **AI**: Google Gemini for document analysis and question answering

## Getting Started

### 1. Install Python dependencies

```bash
pip install -r requirements.txt
```

### 2. Set up environment variables

Create a `.env` file and add your Google API key:

```env
GOOGLE_API_KEY=your_google_api_key_here
```

### 3. Start the FastAPI backend server

```bash
uvicorn main:app --reload
```

The backend will be available at `http://localhost:8000`

### 4. Install and run the React frontend

In a new terminal, navigate to the frontend directory:

```bash
cd frontend
npm install
npm start
```

The frontend will be available at `http://localhost:3000`

### 5. Access the application

Open your browser and go to:

- **React Frontend**: `http://localhost:3000` (recommended)
- **Legacy HTML Interface**: `http://localhost:8000` (fallback)

## Usage

1. **Upload Document**: Use the sidebar to select and upload a PDF document
2. **Process**: Click "Process Documents" and wait for completion
3. **Analyze**: View extracted clauses categorized by risk level
4. **Chat**: Ask questions about your document in the chat interface
5. **Navigate**: Click page references to jump to specific sections in the PDF
   viewer

## Development

### Backend Development

- FastAPI server with auto-reload: `uvicorn main:app --reload`
- API documentation: `http://localhost:8000/docs`

### Frontend Development

- React development server: `npm start` (in frontend directory)
- Hot reload enabled for development
- Tailwind CSS for styling

### Project Structure

```
├── main.py                 # FastAPI backend
├── requirements.txt        # Python dependencies
├── static/                 # Legacy HTML interface
├── uploads/               # Uploaded PDF storage
├── faiss_index/          # Vector database
└── frontend/             # React application
    ├── src/
    │   ├── components/   # React components
    │   ├── services/     # API service layer
    │   └── App.js       # Main application
    └── package.json     # Node.js dependencies
```

## API Endpoints

- `POST /upload-pdf/` - Upload and process PDF documents
- `GET /progress/` - Check processing progress
- `POST /ask-question/` - Ask questions about uploaded documents
- `GET /clauses/` - Retrieve analyzed clauses with filters
- `GET /metadata/` - Get document metadata

## Deployment

### Backend Deployment

- Deploy FastAPI on platforms like Railway, Render, Heroku, or any cloud VM
- Set environment variables in your deployment platform
- Use `python main.py` for production (not uvicorn with reload)

### Frontend Deployment

- Build React app: `npm run build` (in frontend directory)
- Deploy built files to any static hosting service (Netlify, Vercel, etc.)
- Update API base URL in `src/services/api.js` for production

### Environment Variables

- `GOOGLE_API_KEY`: Required for AI document analysis
- `PORT`: Optional, defaults to 8000 for backend

## License

MIT

# AI-Sprint-2.0
