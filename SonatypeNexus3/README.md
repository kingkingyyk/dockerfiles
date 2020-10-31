# Sonatype Nexus 3 for Raspberry Pi

## Extra Tweaks Applied
- JVM memory limited to 384MB
- JNA 5.6 included

## Build Image
Run 
```
git clone https://github.com/kingkingyyk/dockerfiles.git
cd dockerfiles/SonatypeNexus3
docker build --tag nexus3-pi:latest .
```

## Persistent Volume
Mount folder to /sonatype-work

## Usage
Docker command:
```
docker run --rm -p 8081:8081 /path/to/work:/sonatype-work nexus3-pi:latest
```
Docker Compose:
```
version: "3.8"
services:
  nexus3:
    image: nexus3-pi:latest
    container_name: nexus3
    volumes:
      - /path/to/work:/sonatype-work
    ports:
      - 8081:8081
```
