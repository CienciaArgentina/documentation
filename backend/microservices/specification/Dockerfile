FROM swaggerapi/swagger-ui:latest
EXPOSE 8080
WORKDIR /swagger
COPY openapi.yaml /docs/openapi.yaml
RUN chmod 775 /docs/openapi.yaml
ENV SWAGGER_JSON "/doc/openapi.yaml"
