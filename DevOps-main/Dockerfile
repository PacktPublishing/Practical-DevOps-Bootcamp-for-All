FROM   ubuntu:24.04

RUN    apt-get -y update && apt-get -y install python3 python3-pip python3.12-venv

WORKDIR /opt

COPY   ./requirements.txt .

RUN    python3 -m venv /opt/devopspython

RUN    /opt/devopspython/bin/pip install --upgrade pip \
      && /opt/devopspython/bin/pip install -r requirements.txt

COPY   ./app.py .

ENV   FLASK_APP=/opt/app.py
ENV   PATH="/opt/devopspython/bin:$PATH"

EXPOSE   8080

CMD   ["flask", "run", "--host=0.0.0.0", "--port=8080"]
