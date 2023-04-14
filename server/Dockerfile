FROM python:3.7-slim
WORKDIR /server
ADD object_detection.py /server
RUN mkdir /server/yolo_tiny_configs
ADD /yolo_tiny_configs/ /server/yolo_tiny_configs
COPY requirements.txt requirements.txt
RUN apt-get update -y && apt-get install -y ffmpeg libsm6 libxext6
RUN pip3 install --upgrade pip
RUN pip3 install -r requirements.txt
CMD ["python", "/server/object_detection.py"]
