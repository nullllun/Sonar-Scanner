FROM java:alpine  
ENV SONAR_SCANNER_VERSION 2.8

RUN apk add --no-cache wget && \  
    apk add --no-cache git && \ 
    wget https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-${SONAR_SCANNER_VERSION}.zip && \  
    unzip sonar-scanner-${SONAR_SCANNER_VERSION} && \  
    cd /usr/bin && ln -s /sonar-scanner-${SONAR_SCANNER_VERSION}/bin/sonar-scanner sonar-scanner && \  
    apk del wget && \
    rm /sonar-scanner-${SONAR_SCANNER_VERSION}.zip && \
    git config --global user.email "you@example.com" && \
    git config --global user.name "Testuser"
