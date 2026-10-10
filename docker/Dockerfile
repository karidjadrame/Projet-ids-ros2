FROM ros:humble-ros-base
RUN apt-get update && apt-get install -y python3-pip tcpdump iproute2 ros-humble-ros2bag ros-humble-rosbag2-storage-default-plugins && rm -rf /var/lib/apt/lists/*
RUN pip3 install --no-cache-dir 'numpy<2' pandas scikit-learn joblib matplotlib
RUN pip3 install --no-cache-dir torch --index-url https://download.pytorch.org/whl/cpu
RUN echo 'source /opt/ros/humble/setup.bash' >> /root/.bashrc
ENV PYTHONPATH=/ws
WORKDIR /ws