# Use Python 3.8 base image
FROM python:3.8

# Set working directory in the container
WORKDIR /app

# Copy all project files into the container
COPY . /app

# Install dependencies from requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Expose the application port
EXPOSE 3111

# Initialize the database with predefined posts
RUN python init_db.py

# Set the default command to run the TechTrends application
CMD ["python", "app.py"]
