
cd ~/gpt-oss-120b-faq

git remote -v

git pull --ff-only teacher main

ls -lh ~/gpt-oss-teacher-faq/models/gpt-oss-120b-MXFP4.gguf

curl http://127.0.0.1:8080/health or 

tmux new -s teacher

~/llama.cpp/build/bin/llama-server --model ~/gpt-oss-teacher-faq/models/gpt-oss-120b-MXFP4.gguf --alias gpt-oss-120b --host 127.0.0.1 --port 8080 --ctx-size 4096 --threads 16 --parallel 1 --n-gpu-layers 0 --jinja

(Detach from tmux using Ctrl+B, then D)

python3 -u scripts/generate_batch.py

wc -l output/teacher_output.jsonl
