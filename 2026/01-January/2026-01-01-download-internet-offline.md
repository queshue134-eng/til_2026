# 2026-01-01 TIL: How to Download the Internet for Offline Access

## Category: Data Hoarding / Digital Preservation

### Video Reference

[![YouTube](https://img.shields.io/badge/YouTube-Video-red?style=flat-square&logo=youtube)](https://www.youtube.com/watch?v=WZC2D38CaVY)

### Key Takeaways

The concept of "downloading the internet" refers to **offline data archiving** — preserving websites, knowledge bases, and digital content for access without an internet connection.

---

## 🤔 Why Download the Internet?

| Reason                    | Use Case                                        |
| ------------------------- | ----------------------------------------------- |
| **Offline Access**        | Remote areas, travel, internet outages          |
| **Digital Preservation**  | Websites disappear; content gets deleted        |
| **Research Archiving**    | Academic resources, documentation               |
| **Disaster Preparedness** | Knowledge access during infrastructure failures |
| **Privacy**               | Access information without tracking             |

---

## 🛠️ Key Tools & Methods

### 1. Wikipedia Offline (Kiwix)

Download the entire Wikipedia for offline browsing.

| Tool          | Description                                |
| ------------- | ------------------------------------------ |
| **Kiwix**     | Offline reader for Wikipedia & other wikis |
| **ZIM files** | Compressed archive format for wikis        |
| **Size**      | ~90GB for English Wikipedia with images    |

### 2. Website Mirroring

Create local copies of entire websites.

| Tool                | Use Case                                     |
| ------------------- | -------------------------------------------- |
| **HTTrack**         | Full website download with link preservation |
| **wget**            | Command-line recursive downloading           |
| **Wayback Machine** | Archive.org's internet archive               |

### 3. Documentation Archives

Offline access to developer documentation.

| Resource        | Tool                                  |
| --------------- | ------------------------------------- |
| **DevDocs**     | Offline-capable documentation browser |
| **Dash/Zeal**   | Documentation browser with docsets    |
| **ReadTheDocs** | Many projects offer downloadable docs |

### 4. Video & Media Archiving

Preserve video content locally.

| Tool              | Purpose                          |
| ----------------- | -------------------------------- |
| **yt-dlp**        | Download videos from 1000+ sites |
| **gallery-dl**    | Image gallery archiving          |
| **Plex/Jellyfin** | Self-hosted media servers        |

---

## 💾 Storage Considerations

| Content Type                    | Approximate Size    |
| ------------------------------- | ------------------- |
| English Wikipedia (text only)   | ~22 GB              |
| English Wikipedia (with images) | ~90 GB              |
| Stack Overflow data dump        | ~50 GB              |
| Project Gutenberg (books)       | ~60 GB              |
| OpenStreetMap (planet)          | ~70 GB (compressed) |

**Total for "essential knowledge":** ~300-500 GB is a reasonable target for a comprehensive offline library.

---

## 📚 Notable Offline Archives

| Archive               | Content                      |
| --------------------- | ---------------------------- |
| **Internet Archive**  | 99+ petabytes of web history |
| **Project Gutenberg** | 70,000+ free ebooks          |
| **LibGen**            | Academic papers & books      |
| **Sci-Hub**           | Research papers              |
| **OpenStreetMap**     | Global map data              |

---

## 🤖 Self-Hosting LLMs (Offline AI)

Run AI models locally without internet dependency.

### Popular Tools

| Tool                      | Description                      |
| ------------------------- | -------------------------------- |
| **Ollama**                | Easy-to-use local LLM runner     |
| **LM Studio**             | GUI for running local models     |
| **llama.cpp**             | Efficient CPU inference for LLMs |
| **text-generation-webui** | Feature-rich web interface       |
| **LocalAI**               | OpenAI-compatible local API      |

### Recommended Models (by VRAM)

| VRAM  | Model                          | Size       |
| ----- | ------------------------------ | ---------- |
| 4GB   | Phi-3 Mini, Gemma 2B           | ~2-4 GB    |
| 8GB   | Llama 3 8B, Mistral 7B         | ~4-8 GB    |
| 16GB  | Llama 3 70B (Q4), Mixtral 8x7B | ~20-40 GB  |
| 24GB+ | Llama 3 70B, Qwen 72B          | ~40-140 GB |

### Quick Start with Ollama

```bash
# Install Ollama
curl -fsSL https://ollama.com/install.sh | sh

# Download and run a model
ollama run llama3

# Run with a specific quantization
ollama run mistral:7b-instruct-q4_K_M
```

### Benefits of Local LLMs

- **Privacy** — Data never leaves your machine
- **No API costs** — Run unlimited queries
- **Offline access** — Works without internet
- **Customization** — Fine-tune for your needs
- **No censorship** — Uncensored model options

---

## ⚠️ Legal & Ethical Considerations

1. **Copyright** — Only archive content you have rights to access
2. **Terms of Service** — Some sites prohibit bulk downloading
3. **Bandwidth** — Be respectful; don't overload servers
4. **Personal Use** — Most archiving is legal for personal, non-commercial use
5. **Preservation Intent** — Digital preservation is a legitimate cultural goal

---

### Additional Resources

- [Kiwix - Offline Wikipedia](https://www.kiwix.org/)
- [Internet Archive](https://archive.org/)
- [HTTrack Website Copier](https://www.httrack.com/)
- [yt-dlp GitHub](https://github.com/yt-dlp/yt-dlp)
- [r/DataHoarder](https://www.reddit.com/r/DataHoarder/)
- [Original Video](https://www.youtube.com/watch?v=WZC2D38CaVY)
