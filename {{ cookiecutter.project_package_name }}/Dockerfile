FROM python:3.10


ARG PROJECT_PACKAGE_NAME={{ cookiecutter.project_package_name }}

ARG WORK_DIR=/code
ARG REQUIREMENTS_FILENAME=requirements.frozen


WORKDIR ${WORK_DIR}


COPY ${REQUIREMENTS_FILENAME} .
RUN pip install -r ${REQUIREMENTS_FILENAME}


COPY ${PROJECT_PACKAGE_NAME} .


CMD python run.py
