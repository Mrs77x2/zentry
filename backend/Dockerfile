# Dockerfile para el backend Zentry

# 1️⃣ Imagen base con Java 17 (necesario para Spring Boot)
FROM eclipse-temurin:17-jdk-alpine

# 2️⃣ Carpeta de trabajo dentro del contenedor
WORKDIR /app

# 3️⃣ Copiar archivos de Maven (pom.xml) primero para cachear dependencias
COPY pom.xml .

# 4️⃣ Instalar dependencias de Maven (sin copiar el código aún)
RUN apk add --no-cache maven \
    && mvn dependency:go-offline

# 5️⃣ Copiar todo el código fuente al contenedor
COPY src ./src

# 6️⃣ Construir el proyecto dentro del contenedor
RUN mvn package -DskipTests

# 7️⃣ Puerto que exponemos para el backend (igual que en tu laptop)
EXPOSE 8080

# 8️⃣ Comando para ejecutar la aplicación
CMD ["java", "-jar", "target/backend-0.0.1-SNAPSHOT.jar"]
