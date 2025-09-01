# Flask API

Modified from here [Simple Flask App with Docker](https://github.com/chesahkalu/Simple-Flask-App-Docker). Approximately the same
code, comments removed and placed in a
separate document.

Keeping the license, thank you very much [Victor](https://github.com/chesahkalu)!

## Running as a server on your host computer

This is for Flask development purposes, if you only need to run
Flask in docker, jump to section **Running with docker**!

### Dependencies with pip

If you use virtual environment you may use

<pre>
mkdir myproject
cd myproject
python3 -m venv .venv
.venv\Scripts\activate
</pre>

(or `. .venv/bin/activate` on Linux)

Then install the necessary packages with:

<pre>
pip install Flask
pip install -U flask-cors
</pre>

### Dependencies with apt

On a Debian based Linux system you may alternatively install
the packages with apt:

<pre>
sudo apt install python3-flask
sudo apt install python3-cors
</pre>

### Running on host

<pre>
python flaskapi.py
</pre>

## Running with docker

For any <i style="background: yellow"><b>n</b></i> 

<pre>
docker build -t flaskapi:v<i style="background: yellow"><b>n</b></i> .
</pre>

<pre>
docker run -d -p 5070:8001 flaskapi:v<i style="background: yellow"><b>n</b></i>
</pre>
