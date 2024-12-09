FROM openjdk:11-jre

# Instalar wget y graphviz
RUN apt-get update && apt-get install -y wget graphviz

# Crear directorio de trabajo
WORKDIR /schemaspy

# Descargar SchemaSpy
RUN wget -O schemaspy.jar https://github.com/schemaspy/schemaspy/releases/download/v6.1.0/schemaspy-6.1.0.jar

# Descargar el driver PostgreSQL
RUN wget -O postgresql.jar https://jdbc.postgresql.org/download/postgresql-42.2.23.jar

# Crear directorio de salida
RUN mkdir /output
WORKDIR /output

# Hacer ejecutable el jar
RUN chmod +x /schemaspy/schemaspy.jar