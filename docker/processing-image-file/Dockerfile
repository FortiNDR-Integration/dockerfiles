
FROM demisto/python3-deb:3.11.10.112166

COPY requirements.txt .

RUN apt-get update && apt-get install -y --no-install-recommends gcc python3-dev libjpeg-dev wget libglib2.0-0 libsm6 libxext6 libgl1-mesa-glx libxrender1 libxrender-dev \
  && pip install --no-cache-dir -r requirements.txt && apt-get purge -y --auto-remove \
  gcc python3-dev \
&& rm -rf /var/lib/apt/lists/*
