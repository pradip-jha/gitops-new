FROM python:3-alpine
COPY requirements.txt .
RUN pip install -r requirements.txt
#RUN addgroup -S appgroup && adduser -S appuser -G appgroup
COPY src /app
EXPOSE 5000
WORKDIR app
# USER appuser
ENTRYPOINT ["python"]
CMD ["hello.py"]
