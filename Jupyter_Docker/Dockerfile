FROM alpine:latest
RUN apk update
RUN apk install build-essential python3.6 python3-pip python3-dev
RUN pip3 -q install pip --upgrade
RUN pip install --upgrade pip
RUN mkdir working_folder
WORKDIR working_folder
COPY . .
RUN python3 helloworld.py
RUN python3 -m pip install -r requirements.txt
RUN python3 -m pip install jupyter
CMD ["jupyter", "notebook", "--port=4321", "--no-browser", "--ip=0.0.0.0", "--allow-root"]




