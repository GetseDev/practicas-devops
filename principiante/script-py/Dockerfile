FROM python:3.9-slim

WORKDIR /app

COPY ./scripts/requirements.txt .

RUN pip install pandas --no-cache-dir -r requirements.txt

COPY ./scripts/** .

ENTRYPOINT ["python"]
CMD ["process_data.py"]

