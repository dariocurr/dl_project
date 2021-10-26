ARG TENSORFLOW_VERSION
FROM tensorflow/tensorflow:${TENSORFLOW_VERSION}

ARG REQUIREMENTS_FOLDER
ARG USER

COPY requirements*.txt ${REQUIREMENTS_FOLDER}

USER root

RUN useradd -ms /bin/bash ${USER}
RUN chown -R ${USER}:${USER} /usr/local/

RUN pip install --upgrade pip
RUN pip install -q \
	-r ${REQUIREMENTS_FOLDER}requirements.txt \
	-r ${REQUIREMENTS_FOLDER}requirements-dev.txt
RUN rm -r ${REQUIREMENTS_FOLDER}

RUN apt update
RUN apt upgrade -y
RUN apt install git -y

USER ${USER}
