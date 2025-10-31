# ollama_streamlit
See the demo code [ollama_client_streamlit.py](https://github.com/sekewei/ollama_streamlit/blob/main/ollama_client_streamlit.py) to [Build a Lightweight Streamlit Client for Local Ollama LLM Interaction](https://seke-blog.blogspot.com/2025/06/building-lightweight-streamlit-client.html).
You will need to install [Ollama](https://ollama.com/download) and download the desired large language models to local site first.
![Demo Screenshot](https://github.com/sekewei/ollama_streamlit/blob/020dbe4aca3b09787c27b4010a9c90d72bbea3d8/ollama_streamlit_demo.jpg)

## FAQ

### How to list repositories shared with me on GitHub?

To view GitHub repositories that have been shared with you (repositories where you've been added as a collaborator):

1. **Via GitHub Web Interface:**
   - Go to [github.com](https://github.com)
   - Click on your profile picture in the top-right corner
   - Select "Your repositories" from the dropdown menu
   - Use the filter dropdown on the left and select "Collaborator" to see repositories where you're a collaborator

2. **Via GitHub CLI:**
   ```bash
   gh repo list --collaborator
   ```
   This will show repositories where you're a collaborator (shared with you).

3. **Via GitHub API:**
   ```bash
   curl -H "Authorization: Bearer YOUR_PERSONAL_ACCESS_TOKEN" https://api.github.com/user/repos?affiliation=collaborator
   ```
   Replace `YOUR_PERSONAL_ACCESS_TOKEN` with your GitHub personal access token.

### How does this app list available Ollama models?

The application automatically detects and lists all Ollama models (LLM repositories) installed on your local machine by calling the Ollama API endpoint `/api/tags`. These models appear in the "model_engine" dropdown in the sidebar. To add more models, use the Ollama CLI:

```bash
ollama pull llama3.1
ollama pull gemma2:9b
```

Then restart the Streamlit app to see the newly installed models in the dropdown.
