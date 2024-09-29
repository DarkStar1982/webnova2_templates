FROM ubuntu:focal
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update
RUN apt-get install vim python3-dev python3-pip -y
RUN useradd -ms /bin/bash user1
WORKDIR /home/user1
RUN mkdir -p /home/user1/mission_config
RUN mkdir -p /home/user1/entry_point
RUN mkdir -p /home/user1/input_queue
RUN mkdir -p /home/user1/output_queue
ADD run_executable.sh /home/user1/entry_point
ADD executable.py /home/user1/entry_point
ADD mission_config1712967621622.json /home/user1/mission_config
WORKDIR /home/user1/entry_point
CMD /home/user1/entry_point/run_executable.sh
