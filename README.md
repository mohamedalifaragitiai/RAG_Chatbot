# RAG-Chatbot
This is professional implementations of the RAG model



## Best command for prompt terminal separtion 
```bash
$ PS1="\[\033[1;34m\]\w\[\033[0m\]\n\[\033[1;32m\]\$\[\033[0m\] "
```
💾 To make it permanent:

Add this line at the end of your ~/.bashrc

```bash
export PS1="\[\033[1;34m\]\w\[\033[0m\]\n\[\033[1;32m\]\$\[\033[0m\] "
```
✅ Correct way (keep virtual environment name visible)

Use the special variable \u (user), \h (hostname), \w (current dir), and include $(...) to keep the virtualenv name dynamically:


```bash
PS1="(\$(basename \$VIRTUAL_ENV 2>/dev/null)) \[\033[1;34m\]\w\[\033[0m\]\n\[\033[1;32m\]\$\[\033[0m\] "

```


## Requirments 
🧠 Step-by-step guide to use Python 3.8 in your project
1️⃣ Check if Python 3.8 is installed

Run:

python3.8 --version


If you get something like:

Python 3.8.x


✅ Great, continue.

If not:

sudo add-apt-repository ppa:deadsnakes/ppa -y
sudo apt update
sudo apt install python3.8 python3.8-venv python3.8-distutils -y


2️⃣ Create a new virtual environment using Python 3.8

Inside your project folder:

cd ~/Projects/rag_course/RAG_Chatbot
python3.8 -m venv rag_venv


That ensures your venv uses Python 3.8 specifically.

3️⃣ Activate it
source rag_venv/bin/activate


Now check:

python --version


✅ Should show:

Python 3.8.x

4️⃣ (Optional) Reinstall dependencies

If you have a requirements.txt:

pip install -r requirements.txt

5️⃣ Verify permanently

Every time you activate this environment, it will use Python 3.8 automatically because it’s bound to that version at creation.

## Ceate a .env 
```bash
$ cp .env .env.example 
```


## Run FastAPI server 

```bash 
$ uvicorn main:app --reload  --host  0.0.0.0 
```


### Postman collection path 
Get postman collection from /home/abuali/Projects/rag_course/RAG_Chatbot/assets

