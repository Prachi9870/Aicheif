# Use Python base image
FROM python:3.10-slim

# Set work directory
WORKDIR /app

# Copy all files to the container
COPY . /app

# Install dependencies
RUN pip install --no-cache-dir flask pandas openpyxl jupyter

# Expose ports for Flask (5000) and Jupyter (8888)
EXPOSE 5000 8888

# Default command to run both Flask and Jupyter if needed
CMD ["sh", "-c", "jupyter notebook --ip=0.0.0.0 --allow-root & python3 scripts.py"]
