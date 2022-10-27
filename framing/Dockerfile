FROM python:3.9
# Set the working directory

RUN apt-get update && apt-get install -y python3 python3-pip python3-opencv wget
RUN pip3 install scikit-learn numpy opencv-python

WORKDIR /work

ADD 20-20000.mp4 /work
ADD split.py /work
ADD run.sh /work

RUN chmod +x /work/run.sh

ENTRYPOINT ["/work/run.sh", "20-20000.mp4" , "data-20-20000"]
