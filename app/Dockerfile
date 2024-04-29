# Use a more recent Alpine image if available
FROM python:3.8-alpine

# Set the working directory inside the container
WORKDIR /app

# Expose the correct port that Flask will run on inside the container
EXPOSE 5001

# Environment variables can be set in the Dockerfile if they are static
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_RUN_PORT=5001


# Copy the rest of the application
COPY ./src .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt


# Use the official command for running Flask applications in production
CMD ["flask", "run"]
