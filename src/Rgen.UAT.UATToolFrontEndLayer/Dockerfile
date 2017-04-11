FROM microsoft/dotnet:1.0.0-preview2-sdk

# Set the Working Directory
WORKDIR /app

# Configure the listening port to 80
ENV ASPNETCORE_URLS http://*:8080
ENV PORT 8080
EXPOSE 8080

# Copy the app
COPY . /app

RUN echo "Application will run on $ASPNETCORE_URLS"

# Restore NuGet Packages
RUN dotnet restore

# Start the app
ENTRYPOINT dotnet run | sleep 5000
