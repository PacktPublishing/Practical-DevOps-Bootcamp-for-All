# Important Steps for reference

Option1: Steps for creating virtual environment using "source"

- apt-get update
- apt-get install python3-pip python3.12-venv
- python3 -m venv devopspython
- source devopspython/bin/activate
- python3 app.py &

Option2: While using source to activate a virtual environment in a Dockerfile is technically possible, it is generally not recommended or necessary for most Python applications within Docker containers. So we will leverage and Install Python dependencies using virtualenv pip:

- apt-get update
- apt-get install python3-pip python3.12-venv
- python3 -m venv devopspython
- /devopspython/bin/pip install -r requirements.txt
- /devopspython/bin/python3 app.py &

Note: Option2 is generally used in Dockerfile for Python application, and we will use the same in one of our demos for containerizing Python application.
