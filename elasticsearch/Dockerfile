ARG ELK_VERSION

# https://github.com/elastic/elasticsearch-docker
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}
ARG ELK_VERSION

#安裝 jieba 分詞 
# RUN curl -L https://services.gradle.org/distributions/gradle-5.4-bin.zip -o gradle-5.4-bin.zip
# RUN mkdir /opt/gradle
# RUN unzip -d /opt/gradle gradle-5.4-bin.zip
# ENV GRADLE_HOME=/opt/gradle/gradle-5.4
# ENV PATH=$PATH:$GRADLE_HOME/bin
# RUN mkdir -p /usr/share/elasticsearch/plugins/jieba
# RUN wget -O elasticsearch-jieba-plugin-6.4.1.zip http://bit.ly/2Y2ZQua && ls && unzip elasticsearch-jieba-plugin-6.4.1.zip && rm elasticsearch-jieba-plugin-6.4.1.zip && cd elasticsearch-jieba-plugin-6.4.1 && gradle pz &&  cp build/distributions/elasticsearch-jieba-plugin-6.4.0.zip /usr/share/elasticsearch/plugins
# RUN cd /usr/share/elasticsearch/plugins && unzip elasticsearch-jieba-plugin-6.4.0.zip && rm elasticsearch-jieba-plugin-6.4.0.zip

#安裝 ik 分詞 
WORKDIR /usr/share/elasticsearch/plugins
RUN wget -O ik.zip https://github.com/medcl/elasticsearch-analysis-ik/releases/download/v${ELK_VERSION}/elasticsearch-analysis-ik-${ELK_VERSION}.zip
RUN ls && unzip -d ./ik ik.zip
# 自行添加字典給ik
RUN cd ik && cd config && curl -o custom.dic https://raw.githubusercontent.com/Mudboyzh/sc-dictionary/master/main.txt
RUN rm ik.zip

