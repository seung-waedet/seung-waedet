## Seung-wa Akpan

Backend & Applied AI Engineer · Python
Abuja, Nigeria (UTC+1), working fully remote.

### Now

Main engineer on [OraScribe](https://orascribe.ai), a transcription and translation platform:
GPU model serving on serverless GPU platforms (Modal, and RunPod before that), Celery job
pipelines, billing, and the evals that test them. The code is private; some of the work:

- Cut LLM cold-start time on staging from 266s to 13-30s in most runs by restoring a saved GPU memory snapshot.
- Tested Qwen3-4B against M2M100 on 15 idioms before building an LLM translation path behind a flag. Word-for-word mistranslations fell from 11 to at most 1.
- Found that the voice activity filter was silently dropping sung speech. After the fix, one 8-minute recording went from 120 to 421 transcribed words.
- Built an eval suite for dropped speech: fast no-GPU tests on every commit, plus a real-GPU run that fails on the old settings.
- Moved 30-100+ minute GPU jobs off a single long-held connection to a submit, poll and reconcile flow behind a rollback flag.

### Public work

- [pidgin-deployment-eval](https://github.com/seung-waedet/pidgin-deployment-eval): can LLMs be trusted with everyday tasks in Nigerian Pidgin? In progress: the item schema and checks are built, no model results yet.
- [document-rag-service](https://github.com/seung-waedet/document-rag-service): a RAG API that ingests PDF, DOCX and TXT files into ChromaDB and answers questions with an LLM. NestJS, LangChain, OpenRouter, Docker.
- [HP Community](https://hpcommunity.app): two live progressive web apps for a faith community, a companion app (about 25 weekly users) and a reading library with full-text search.

### Stack

Python, Flask, FastAPI, Celery, Redis, vLLM, Whisper, PostgreSQL, Docker, pytest.
Also Node.js, TypeScript, NestJS, MongoDB.

### Contact

[seungwaakpan.com](https://www.seungwaakpan.com) ·
[LinkedIn](https://www.linkedin.com/in/seungwaakpan) ·
seungwaakpan@gmail.com
