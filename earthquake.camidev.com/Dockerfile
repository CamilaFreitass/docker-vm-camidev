FROM python:3.10.2
ENV PYTHONUNBUFFERED 1
ARG CHAVE_GOOGLE_MAPS


WORKDIR /app/earthquake
RUN git clone https://github.com/CamilaFreitass/earthquake.git /app/earthquake
RUN pip install -r /app/earthquake/requirements.txt
RUN python make.py $CHAVE_GOOGLE_MAPS


EXPOSE 8000
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]