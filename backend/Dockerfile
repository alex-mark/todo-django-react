FROM python:3
ENV PYTHONUNBUFFERED 1
ENV WORKDIR /code/

RUN pip install --upgrade pip pipenv setuptools wheel
RUN mkdir ${WORKDIR}
WORKDIR ${WORKDIR}
COPY Pipfile Pipfile.lock ${WORKDIR}
RUN pipenv install --deploy --system --ignore-pipfile
COPY . ${WORKDIR}