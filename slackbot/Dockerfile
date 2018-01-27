FROM python:2
WORKDIR /usr/src/app
RUN git clone https://github.com/kajakdc/infotv-info-ukko.git .
RUN pip install --no-cache-dir -r requirements.txt
CMD ["python", "main.py"]
