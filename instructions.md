# Installation & Setup Guide

This project is fully containerized using Docker to ensure that the K-Means clustering, Pareto analysis, and unit economic models run exactly as intended, regardless of your local operating system or Python configuration.

Follow these steps to clone the repository and launch the strategic audit environment.

1. Prerequisites

Before starting, ensure you have the following installed on your machine:

- Git
- Docker Desktop:

2. Clone the Repository

Open your terminal (or Command Prompt/PowerShell) and run:

```Bash

git clone https://github.com/machaniG/retention_analysis.git
cd retention_analysis
```

3. Build the Docker Image

The Dockerfile contains the "recipe" for the environment, including Python 3.11 and all necessary libraries (pandas, scikit-learn, matplotlib). Run the following command to build the image:

```Bash

docker build -t growth-operations-strategy .
Note: The first build may take a few minutes as it downloads the base Python image and installs dependencies.
```

4. Run the Project

Once the build is complete, launch the container. This command maps the container's Jupyter port (8888) to your local machine:

```Bash

docker run -p 8888:8888 growth-operations-strategy 
```

5. Accessing the Notebooks

After running the command above, your terminal will display a series of logs. Look for a URL that looks like this:

http://127.0.0.1:8888/?token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

Copy the URL (including the token).

Paste it into your web browser.

You will now have access to the Jupyter interface containing the project core analysis files:

