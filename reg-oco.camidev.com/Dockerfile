FROM python:3.10.2
ENV PYTHONUNBUFFERED 1
WORKDIR /app/reg-oco
RUN git clone https://github.com/CamilaFreitass/registro_ocorrencias.git /app/reg-oco
RUN pip install -r /app/reg-oco/requirements.txt


RUN echo "SECRET_KEY=sua_chave_aqui" >> /app/reg-oco/.env && \
    echo "DEBUG=True" >> /app/reg-oco/.env && \
    echo "environment=False" >> /app/reg-oco/.env && \
    echo "ALLOWED_HOSTS=localhost" >> /app/reg-oco/.env

WORKDIR /app/reg-oco/temp
RUN python /app/reg-oco/manage.py migrate

EXPOSE 8000
CMD ["python", "/app/reg-oco/manage.py", "runserver", "0.0.0.0:8000"]