# Official lightweight Python image
FROM python:3.11-slim

# Set working directory inside container
WORKDIR /app

# Copy dependencies and install
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy dataset and Python application
COPY data.csv .
COPY train_and_predict.py .

# Create output directory
RUN mkdir -p /app/output

# Run ML training application
CMD ["python", "train_and_predict.py"]
