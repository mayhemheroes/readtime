FROM python:3.11-slim
RUN apt-get update && apt-get install -y clang && rm -rf /var/lib/apt/lists/*
RUN pip3 install atheris

COPY . /readtime
WORKDIR /readtime
RUN python3 -m pip install -r requirements.txt && python3 -m pip install . && chmod +x fuzz/readtime_markdown_fuzz.py

ENTRYPOINT [ ]
CMD ["/readtime/fuzz/readtime_markdown_fuzz.py"]
